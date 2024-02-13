<template>
  <nav class="filter-nav">
    <button @click="updateFilter('all')" :class="{ active: current === 'all' }">View all</button>
    <button @click="updateFilter('completed')" :class="{ active: current === 'completed' }">
      Completed
    </button>
    <button @click="updateFilter('ongoing')" :class="{ active: current === 'ongoing' }">
      Ongoing
    </button>
  </nav>
</template>

<script>
export default {
  props: ['current'],
  methods: {
    updateFilter(by) {
      this.$emit('filterChange', by);
    },
  },
};
</script>

<style>
.filter-nav button {
  margin-right: 10px;
  border: none;
  outline: none;
  color: #bbb;
  font-weight: bold;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 1px;
  cursor: pointer;
  background: none;
}
.filter-nav button.active {
  color: #555;
}
</style>
