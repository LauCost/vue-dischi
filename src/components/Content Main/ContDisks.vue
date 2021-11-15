<template>
  <div class="container">
    <Disk
      v-for="disk in disks.response"
      :key="disk.id"
      :image="disk.poster"
      :titolo="disk.title.toUpperCase()"
      :autore="disk.author"
      :anno="disk.year"
    />
  </div>
</template>


<script>
import axios from "axios";
import Disk from "./Disk.vue";

export default {
  data() {
    return {
      disks: [],
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((r) => {
        console.log(r.data);

        this.disks = r.data;
      })
      .catch((e) => {
        console.log(e, "ops");
      });
  },

  components: {
    Disk,
  },
};
</script>


<style lang="scss">
.container {
  padding: 120px 0;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
</style>