<template>
  <nav v-if="showNavbar" class="navbar is-fixed-top" role="navigation">
    <modal :component="modalComp" @exitModal="closeModal" />

    <div class="navbar-brand">
      <router-link class="navbar-item" to="/" exact>
        <!-- <img src="/static/yourLogo.png" alt="Your Logo" width="112" height="28"> -->
        <h1 id="logo">Aao</h1>
      </router-link>

      <div
        :class="{ 'is-active': showMobileNav }"
        class="navbar-burger burger"
        @click="toggleMobileNav"
      >
        <span />
        <span />
        <span />
      </div>
    </div>

    <div
      id="navMenu"
      :class="{ 'is-active': showMobileNav }"
      class="navbar-menu"
    >
      <div class="navbar-start">
        <router-link v-if="isAdmin" to="/accounts" class="navbar-item"
        >Accounts</router-link
        >
      </div>

      <div class="navbar-end">
        <span v-if="!isLoggedIn" class="navbar-item">
          <a class="navbar-item button accNav is-info" @click="openSignup()">
            Sign Up</a
          >
          <a class="navbar-item button accNav" @click="openLogin()">Log In</a>
        </span>

        <div v-if="isLoggedIn" class="navbar-item has-dropdown is-hoverable">
          <a class="navbar-link is-active"> Account </a>
          <div class="navbar-dropdown">
            <router-link to="/account" class="navbar-item">
              Overview
            </router-link>
            <hr class="navbar-divider" >
            <div class="navbar-item">
              <div>
                <small>
                  <a data-no-instant @click="logout()">Sign Out</a>
                </small>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
import { get } from "vuex-pathify"

export default {
  name: "Navbar",
  components: {},
  mixins: [],
  data() {
    return {
      modalComp: null,
      showMobileNav: false,
    }
  },
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  computed: {
    showNavbar: get("ui/showNavbar"),
    isLoggedIn: get("account/isAuthenticated"),
    userRole: get("account/userRole"),
    isAdmin: function () {
      return this.userRole === "ADMIN"
    },
  },
  methods: {
    closeModal() {
      this.modalComp = null
    },
    openSignup() {
      this.modalComp = () => import("@/components/signup-form")
    },
    openLogin() {
      this.modalComp = () => import("@/components/login-form")
    },
    logout() {
      this.$accountAPI.logout()
      this.$buefy.toast.open({
        duration: 1000,
        message: "Signed Out",
        position: "is-top",
        type: "is-dark",
      })
      this.$router.push("/")
    },
    toggleMobileNav() {
      this.showMobileNav = !this.showMobileNav
    },
  },
  beforeUpdate() {},
  updated() {},
  beforeDestroy() {},
}
</script>

<style lang="scss">
nav {
  border-bottom: 1px solid $primary;
  right: 0;
  left: 0;
  z-index: 9;
  height: $stickyNavHeight;
}

.navbar-brand,
.navbar-tabs {
  min-height: 0;
  height: $stickyNavHeight;
}

#logo {
  font-weight: 700;
  font-size: 1.5em;
  color: $primary;
}

.is-active {
  .accNav {
    margin: 5px;
  }
}

.accNav {
  margin-left: 5px;
}
</style>
