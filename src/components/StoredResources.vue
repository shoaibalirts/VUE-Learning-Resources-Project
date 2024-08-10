<template>
  <ul v-for="resource in resources" :key="resource.id">
    <learning-resource
      :title="resource.title"
      :id="resource.id"
      :description="resource.description"
      :link="resource.link"
    ></learning-resource>
  </ul>
</template>
<script>
import LearningResource from './LearningResource.vue';
export default {
  components: {
    LearningResource,
  },
  inject: ['resources'], // we have changed from props to inject
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
