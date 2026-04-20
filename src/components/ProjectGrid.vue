<template>
  <section class="project-grid">
    <ProjectSingle
      v-for="project in projects"
      :key="project.title"
      :date="project.date"
      :status="project.status"
      :description="project.description"
      :url="project.url"
      :framework="project.framework"
      :title="project.title"
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
.project-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
  margin-top: 8px;
}

@media (max-width: 900px) {
  .project-grid {
    grid-template-columns: 1fr;
    gap: 20px;
  }
}
</style>