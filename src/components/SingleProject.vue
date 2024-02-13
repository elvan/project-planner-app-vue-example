<template>
  <div class="project">
    <div class="actions">
      <h3 @click="showDetails = !showDetails">{{ project.title }}</h3>
    </div>
    <div v-if="showDetails" class="details">
      <p>{{ project.details }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['project'],
  data() {
    return {
      showDetails: false,
    };
  },
};
</script>

<style scoped>
.project {
  margin: 20px auto;
  padding: 10px 20px;
  border-left: 4px solid #e90074;
  border-radius: 4px;
  background: white;
  box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.05);
}
h3 {
  cursor: pointer;
}
</style>
