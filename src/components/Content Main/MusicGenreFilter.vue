<template>
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