<template>
  <div class="resume-wrap">
    <div class="resume-card">
      <div class="top-row">
        <div>
          <p class="label">Profile</p>
          <h2>Ogungbade Femi</h2>
        </div>
        <p class="role">Frontend Developer</p>
      </div>

      <p class="summary">
        Frontend developer focused on building responsive, conversion-friendly,
        and maintainable web interfaces with Vue and React.
      </p>

      <div class="divider"><span></span></div>

      <section class="resume-section">
        <h3>Core Skills</h3>
        <p>
          Vue.js, React, JavaScript, TypeScript, HTML5, CSS3, Responsive UI,
          Component Architecture, API Integration
        </p>
      </section>

      <section class="resume-section">
        <h3>Project Highlights</h3>
        <ul>
          <li v-for="project in projects" :key="project.title">
            <strong>{{ project.title }}:</strong> {{ project.description }}
          </li>
        </ul>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    projects: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style scoped>
.resume-wrap {
  display: block;
}

.resume-card {
  border: 1px solid rgba(148, 163, 184, 0.24);
  border-radius: 18px;
  background: rgba(15, 23, 42, 0.62);
  padding: 24px;
}

.top-row {
  display: flex;
  justify-content: space-between;
  gap: 14px;
  align-items: center;
  flex-wrap: wrap;
}

.label {
  color: #22d3ee;
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.72rem;
  margin-bottom: 8px;
}

h2 {
  font-size: clamp(1.4rem, 2.5vw, 1.9rem);
}

.role {
  color: #93c5fd;
}

.summary {
  margin-top: 14px;
  color: #94a3b8;
  line-height: 1.7;
}

.divider {
  margin: 20px 0;
}

.divider span {
  display: block;
  width: 100%;
  height: 1px;
  background: rgba(148, 163, 184, 0.22);
}

.resume-section {
  margin-top: 16px;
}

.resume-section h3 {
  font-size: 1rem;
  margin-bottom: 8px;
}

.resume-section p,
.resume-section li {
  color: #94a3b8;
  line-height: 1.7;
}

ul {
  list-style: none;
  display: grid;
  gap: 10px;
}

strong {
  color: #e2e8f0;
}
</style>
