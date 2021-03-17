<template>
  <div id="app">
    <!-- <GlobalNavbar /> -->
    <transition name="fadePage" mode="out-in">
      <router-view id="appContent" :key="$route.fullPath" />
    </transition>
    <!-- <GlobalFooter /> -->
  </div>
</template>

<script>
import GlobalNavbar from "@/components/navbar-comp"

export default {
  name: "App",
  components: {
    // GlobalNavbar,
    // GlobalFooter: () => import("@/components/footer-comp"),
  },
  mixins: [],
  data() {
    return {}
  },
  beforeCreate() {},
  created() {},
  beforeMount() {},
  mounted() {},
  computed: {},
  methods: {},
  filters: {},
  beforeUpdate() {},
  updated() {},
  beforeDestroy() {},
}
</script>

<style lang="scss">
// setting Buefy variables from the _variables.scss file
@import "~bulma/sass/utilities/_all";
$primary-invert: findColorInvert($primary);
$colors: (
  "white": (
    $white,
    $black,
  ),
  "black": (
    $black,
    $white,
  ),
  "light": (
    $light,
    $light-invert,
  ),
  "dark": (
    $dark,
    $dark-invert,
  ),
  "primary": (
    $primary,
    $primary-invert,
  ),
  "info": (
    $info,
    $info-invert,
  ),
  "success": (
    $success,
    $success-invert,
  ),
  "warning": (
    $warning,
    $warning-invert,
  ),
  "danger": (
    $danger,
    $danger-invert,
  ),
);
$link: $primary;
$link-invert: $primary-invert;
$link-focus-border: $primary;
@import "~bulma";
@import "~buefy/src/scss/buefy";
#app {
  background-color: black !important;
  color: wheat;
}

.title {
  font-weight: 400 !important;
  color: wheat !important;
}

.subtitle {
  color: wheat !important;
  font-size: 0.9rem !important;
  margin-top: -1.4555rem !important;
}
.buttons {
  justify-content: center !important;
  .buttons:not(:last-child) {
    margin-bottom: 0 !important;
  }
}
#app {
  min-height: 100vh !important;
}
.column {
  padding-top: 0 !important;
  padding-bottom: 0 !important;
}

.columns:last-child {
  margin-bottom: 0px !important;
}

.columns {
  margin: 0px !important;
}

.buttons:not(:last-child) {
  margin-bottom: 0px !important;
}

li {
  padding: 0;
  margin: 0;
}

ul {
  counter-reset: index;
  max-height: 100vh;
  overflow-y: auto;
  max-width: 550px;
  margin: auto !important;
}

li {
  justify-content: center;
  counter-increment: index;
  display: flex;
  align-items: center;
  padding: 12px 0 !important;
  box-sizing: border-box;
}

li::before {
  content: "00 AM -- : -- 00 PM";
  font-size: 0.8rem;
  text-align: center;
  font-weight: bold;
  min-width: 50px;
  max-width: 60px;
  padding-right: 12px;
  font-variant-numeric: tabular-nums;
  align-self: flex-start;
  background-image: linear-gradient(to bottom, aquamarine, orangered);
  background-attachment: fixed;
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
}

li + li {
  border-top: 1px solid rgba(255, 255, 255, 0.2);
}

li img {
  margin: 5px;
  width: 45px;
}

ul.blurr > li {
  -webkit-filter: blur(5px);
  -moz-filter: blur(5px);
  -o-filter: blur(5px);
  -ms-filter: blur(5px);
  filter: blur(5px);
  // width: 100px;
  // height: 100px;
  background-color: transparent;

}
</style>
