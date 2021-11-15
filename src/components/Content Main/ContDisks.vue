<template>
  <div class="container">
    <Disk
      v-for="disco in disks.response"
      :key="disco.id"
      :image="disco.poster"
      :titolo="disco.title.toUpperCase()"
    />
    <!-- <div v-for="disk in disks" :key="disk.id">
      <img :src="disk.poster" alt="" />
      <h2>{{ disk.title }}</h2>
    </div> -->
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
  padding-top: 150px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
</style>