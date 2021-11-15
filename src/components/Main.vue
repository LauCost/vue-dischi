<template>
  <main>
    <ContDisks />
  </main>
</template>

<script>
import ContDisks from "./Content Main/ContDisks.vue";
export default {
  components: {
    ContDisks,
  },
};
</script>

<style lang="scss">
main {
  background-color: #1e2d3b;
  height: calc(100vh - 81.6px);
}
</style>