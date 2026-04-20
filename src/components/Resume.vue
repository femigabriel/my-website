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

      <div class="contact-grid">
        <a href="mailto:timfemi@gmail.com">timfemi@gmail.com</a>
        <a href="tel:+2349061513696">+234 906 151 3696</a>
        <a href="https://www.linkedin.com/in/gabriel-oluwafemi" target="_blank" rel="noreferrer">
          linkedin.com/in/gabriel-oluwafemi
        </a>
      </div>

      <p class="summary">
        Front-End Developer with 3+ years of experience building responsive,
        high-performance web applications with React, Next.js, Vue, and modern
        JavaScript frameworks. Proven strength in translating UI/UX designs into
        scalable components, optimizing performance, and delivering products
        that drive engagement and measurable business value.
      </p>

      <div class="divider"><span></span></div>

      <section class="resume-section">
        <h3>Core Skills</h3>
        <p>
          JavaScript (ES6+), TypeScript, HTML5, CSS3, Sass, React.js, Next.js,
          Vue.js, Nuxt.js, TailwindCSS, Node.js, Express.js, REST APIs, Git,
          Vercel, Figma, performance optimization, responsive design.
        </p>
      </section>

      <section class="resume-section">
        <h3>Experience</h3>
        <ul>
          <li>
            <strong>Front-End Developer, Bles Software (Remote)</strong>
            <span>Dec 2023 - Present</span>
          </li>
          <li>
            Built scalable responsive interfaces with React and TailwindCSS,
            integrated REST APIs, and improved load performance with reusable
            component architecture.
          </li>
          <li>
            <strong>Front-End Developer, Charisol (Lagos)</strong>
            <span>Feb 2020 - Dec 2023</span>
          </li>
          <li>
            Developed websites, dashboards, and landing pages from concept to
            deployment; refactored legacy codebases and improved cross-device UX.
          </li>
          <li>
            <strong>Front-End Developer Intern, StarTimes (Lagos)</strong>
            <span>Jan 2019 - Jan 2020</span>
          </li>
          <li>
            Built user-friendly pages with HTML, CSS, and JavaScript while
            supporting debugging, testing, and on-time feature delivery.
          </li>
        </ul>
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

.contact-grid {
  margin-top: 10px;
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.contact-grid a {
  border: 1px solid rgba(148, 163, 184, 0.2);
  border-radius: 999px;
  padding: 4px 10px;
  font-size: 0.78rem;
  color: #cbd5e1;
  text-decoration: none;
}

.contact-grid a:hover {
  border-color: rgba(34, 211, 238, 0.55);
  color: #bff7ff;
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
  gap: 8px;
}

strong {
  color: #e2e8f0;
}

li span {
  display: block;
  color: #67e8f9;
  font-size: 0.82rem;
}
</style>
