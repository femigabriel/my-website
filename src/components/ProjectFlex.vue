<template>
  <section class="featured-grid">
    <ProjectSingle
      v-for="project in projects"
      :key="project.title"
      :description="project.description"
      :url="project.url"
      :framework="project.framework"
      :title="project.title"
      :status="project.status"
      :date="project.date"
      :highlight="project.highlight"
    />
  </section>
</template>

<script>
import ProjectSingle from "./ProjectSingle.vue";

export default {
  components: { ProjectSingle },
  props: {
    projects: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style scoped>
.featured-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
  margin-bottom: 24px;
}

@media (max-width: 900px) {
  .featured-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
}
</style>