<template>
  <div>
    <section class="section">
      <div class="container">
        <div class="columns is-mobile">
          <div class="column">
            <h1 class="title is-size-2">🄰🄰🄾</h1>
            <h2 class="subtitle is-size-5">𝗟𝗲𝘁❜𝘀 𝗽𝗹𝗮𝘆 𝗳𝗲𝘄 𝗴𝗮𝗺𝗲𝘀 𝘁𝗼𝗱𝗮𝘆.</h2>
            <div class="buttons">
              <a class="button is-danger is-small" href="#">JOIN & BOOK SLOTS FREE</a>
              <a class="button is-small" href="#">READ FAQs</a>
            </div>
          </div>
        </div>
        <ul>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
          <li>
            <img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img
              src="https://via.placeholder.com/50/FFDD57/000000?text=%2b"
            ><img src="https://via.placeholder.com/50/FFDD57/000000?text=%2b" >
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "Index",
  components: {},
  mixins: [],
  data() {
    return {
      data: [
        {
          id: 1,
          first_name: "DOT",
          last_name: "GHOST",
          date: "NINJA",
          gender: "KNIG",
        },
        {
          id: 2,
          first_name: "PAN",
          last_name: "TIN",
          date: "SEN",
          gender: "GOL",
        },
        {
          id: 3,
          first_name: "GOU",
          last_name: "TIH",
          date: "NOJ",
          gender: "LPK",
        },
        {
          id: 4,
          first_name: "KIJ",
          last_name: "AWS",
          date: "RTG",
          gender: "NHJ",
        },
        {
          id: 5,
          first_name: "IJK",
          last_name: "LKJ",
          date: "WER",
          gender: "GHJ",
        },
      ],
      columns: [
        {
          field: "first_name",
          // label: "P#1",
        },
        {
          field: "last_name",
          // label: "P#2",
        },
        {
          field: "date",
          // label: "P#3",
          centered: true,
        },
        {
          field: "gender",
          // label: "P#4",
        },
      ],
    }
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

<style lang="scss" scoped></style>
