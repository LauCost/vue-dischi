<template>
  <div>
    <Disk
      v-for="disco in disks"
      :key="disco.id"
      :image="disco.poster"
      :titolo="disco.title"
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