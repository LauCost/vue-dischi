<template>
  <div class="cont_filter">
    <p>FILTER DISKS BY GENRE</p>
    <select
      v-model="filter"
      @change="$emit('filter-genre', filter)"
      name="type"
      id="type"
    >
      <option value="All">All</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      filter: "All",
    };
  },
};
</script>


<style lang="scss">
.cont_filter {
  display: flex;
  justify-content: center;
  padding: 50px 0 0 0;

  p {
    color: white;
    font-size: 40px;
    margin-right: 20px;
  }

  select {
    width: 5%;
    font-size: 30px;
  }
}
</style>