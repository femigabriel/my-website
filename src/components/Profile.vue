<template>
  <aside class="profile-page">
    <div class="profile-content">
      <div class="profile-head">
        <img src="../images/fm.png" alt="Ogungbade Femi" />
        <div class="identity">
          <p class="availability">Available for roles</p>
          <h1>Ogungbade Femi</h1>
          <p>Frontend Developer</p>
        </div>
      </div>

      <p class="about">
        Frontend Developer with 3+ years of experience building responsive,
        high-performance web applications using React, Next.js, Vue, and Nuxt.
        I transform UI/UX ideas into scalable products that improve user
        engagement and business outcomes.
      </p>

      <div class="meta-list">
        <p><i class="las la-map-marker"></i> Lagos, Nigeria</p>
        <p><i class="las la-envelope"></i> timfemi@gmail.com</p>
      </div>

      <div class="skills-box">
        <p class="skills-title">Core Skills</p>
        <div class="skills-grid">
          <span v-for="skill in skills" :key="skill">{{ skill }}</span>
        </div>
      </div>

      <ul class="nav-list">
        <li
          v-for="li in lists"
          :key="li.id"
          :class="['nav-item', { active: li.id === activeId }]"
          @click="setActivePage(li.id)"
        >
          <span>{{ li.numb }}</span>
          <p>{{ li.status }}</p>
        </li>
      </ul>
    </div>

    <div class="social-wrap">
      <a href="https://github.com/femigabriel" target="_blank" rel="noreferrer">
        <i class="lab la-github"></i> GitHub
      </a>
      <a
        href="https://www.linkedin.com/in/gabriel-oluwafemi"
        target="_blank"
        rel="noreferrer"
      >
        <i class="lab la-linkedin"></i> LinkedIn
      </a>
      <a href="https://twitter.com/FemiGab2018" target="_blank" rel="noreferrer">
        <i class="lab la-twitter"></i> Twitter
      </a>
    </div>
  </aside>
</template>

<script>
export default {
  props: ["activeId"],
  data() {
    return {
      lists: [
        { id: 0, numb: "01", status: "PROJECTS" },
        { id: 1, numb: "02", status: "RESUME" },
      ],
      skills: [
        "HTML5",
        "JavaScript",
        "React",
        "TypeScript",
        "Next.js",
        "Vue.js",
        "Nuxt.js",
      ],
    };
  },
  methods: {
    setActivePage(value) {
      this.$emit("setActivePage", value);
    },
  },
};
</script>

<style scoped>
.profile-page {
  min-height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 28px;
}

.profile-content {
  display: grid;
  gap: 16px;
}

.profile-head {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 20px;
}

.profile-head img {
  width: 80px;
  height: 80px;
  border-radius: 18px;
  object-fit: cover;
  border: 1px solid rgba(148, 163, 184, 0.35);
}

.availability {
  color: #67e8f9;
  font-size: 0.75rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.profile-head h1 {
  font-size: 1.55rem;
  line-height: 1.2;
  margin-top: 4px;
}

.identity p:last-child {
  color: #22d3ee;
  margin-top: 4px;
  font-size: 0.92rem;
}

.about {
  color: #94a3b8;
  line-height: 1.75;
}

.meta-list {
  display: grid;
  gap: 8px;
}

.meta-list p {
  color: #b7c4d7;
  font-size: 0.9rem;
  display: inline-flex;
  align-items: center;
  gap: 8px;
}

.skills-box {
  padding: 12px;
  border-radius: 12px;
  border: 1px solid rgba(148, 163, 184, 0.2);
  background: rgba(15, 23, 42, 0.45);
}

.skills-title {
  color: #93c5fd;
  font-size: 0.8rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 10px;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.skills-grid span {
  background: rgba(34, 211, 238, 0.1);
  border: 1px solid rgba(34, 211, 238, 0.3);
  color: #bff7ff;
  font-size: 0.8rem;
  padding: 4px 10px;
  border-radius: 999px;
}

.nav-list {
  list-style: none;
  display: grid;
  gap: 12px;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 12px 14px;
  border: 1px solid rgba(148, 163, 184, 0.18);
  border-radius: 12px;
  color: #a8b6cc;
  cursor: pointer;
  transition: all 0.25s ease;
}

.nav-item span {
  font-size: 0.78rem;
  letter-spacing: 0.14em;
}

.nav-item p {
  letter-spacing: 0.08em;
  font-size: 0.82rem;
}

.nav-item:hover,
.nav-item.active {
  color: #e2e8f0;
  border-color: rgba(34, 211, 238, 0.5);
  background: rgba(34, 211, 238, 0.08);
}

.social-wrap {
  display: grid;
  gap: 10px;
  margin-top: 20px;
}

.social-wrap a {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: #cbd5e1;
  text-decoration: none;
  font-size: 0.93rem;
}

.social-wrap a:hover {
  color: #22d3ee;
}

.lab {
  font-size: 1.1rem;
}

@media (max-width: 1080px) {
  .profile-page {
    gap: 20px;
  }

  .profile-content {
    gap: 14px;
  }
}

@media (max-width: 640px) {
  .profile-page {
    padding: 18px;
  }

  .social-wrap {
    display: none;
  }
}
</style>
