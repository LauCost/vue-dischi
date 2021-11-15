<template>
  <div id="app">
    <Footer />
    <Main />
  </div>
</template>

<script>
import Footer from "./components/Footer.vue";
import Main from "./components/Main.vue";

/* import axios from "axios"; */
export default {
  name: "App",
  components: {
    Footer,
    Main,
  },

  /* mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((r) => {
        console.log(r);
      })
      .catch((e) => {
        console.log(e, "ops");
      });
  }, */
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
