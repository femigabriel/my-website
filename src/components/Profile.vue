<template>
  <aside class="profile-panel">
    <div class="profile-content">
      <div class="profile-head">
        <div class="avatar-wrapper">
          <img src='../images/fm.png' alt="Ogungbade Femi" />
          <div class="online-dot"></div>
        </div>
        <div class="identity">
          <p class="availability">Available for roles</p>
          <h1>Ogungbade Femi</h1>
          <p class="role">Frontend Developer</p>
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
          <span class="nav-number">{{ li.numb }}</span>
          <p class="nav-status">{{ li.status }}</p>
          <div class="nav-glow"></div>
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
.profile-panel {
  background: var(--bg-panel);
  backdrop-filter: blur(16px);
  border: 1px solid var(--border-light);
  border-radius: 28px;
  padding: 28px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: fit-content;
  position: sticky;
  top: 28px;
  transition: transform var(--transition-smooth), box-shadow var(--transition-smooth);
}

.profile-panel:hover {
  box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.3);
  border-color: rgba(34, 211, 238, 0.25);
}

.profile-content {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.profile-head {
  display: flex;
  align-items: center;
  gap: 16px;
}

.avatar-wrapper {
  position: relative;
}

.profile-head img {
  width: 85px;
  height: 85px;
  border-radius: 24px;
  object-fit: cover;
  border: 2px solid rgba(34, 211, 238, 0.5);
  box-shadow: 0 8px 20px -6px rgba(0, 0, 0, 0.4);
  transition: transform var(--transition-fast);
}

.profile-head img:hover {
  transform: scale(1.02);
}

.online-dot {
  position: absolute;
  bottom: 4px;
  right: 4px;
  width: 14px;
  height: 14px;
  background-color: #10b981;
  border-radius: 50%;
  border: 2px solid var(--bg-panel);
  animation: pulse 2s infinite;
}

@keyframes pulse {
  0% { opacity: 1; transform: scale(1); }
  50% { opacity: 0.7; transform: scale(1.1); }
  100% { opacity: 1; transform: scale(1); }
}

.availability {
  color: var(--accent-cyan);
  font-size: 0.7rem;
  font-weight: 500;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  background: rgba(34, 211, 238, 0.1);
  display: inline-block;
  padding: 2px 8px;
  border-radius: 20px;
  width: fit-content;
}

.profile-head h1 {
  font-size: 1.65rem;
  font-weight: 600;
  line-height: 1.2;
  margin-top: 8px;
  letter-spacing: -0.02em;
}

.role {
  color: var(--accent-blue);
  font-size: 0.9rem;
  margin-top: 6px;
  font-weight: 500;
}

.about {
  color: var(--text-secondary);
  line-height: 1.6;
  font-size: 0.9rem;
}

.meta-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 8px 0;
}

.meta-list p {
  color: #cbd5e1;
  font-size: 0.85rem;
  display: inline-flex;
  align-items: center;
  gap: 10px;
  background: rgba(255, 255, 255, 0.03);
  padding: 6px 12px;
  border-radius: 40px;
  width: fit-content;
}

.skills-box {
  padding: 18px 16px;
  border-radius: 20px;
  background: rgba(15, 23, 42, 0.6);
  border: 1px solid var(--border-light);
}

.skills-title {
  color: var(--accent-blue);
  font-size: 0.7rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  margin-bottom: 14px;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.skills-grid span {
  background: rgba(34, 211, 238, 0.08);
  border: 1px solid rgba(34, 211, 238, 0.2);
  color: #bff7ff;
  font-size: 0.75rem;
  font-weight: 500;
  padding: 6px 14px;
  border-radius: 40px;
  transition: all var(--transition-fast);
}

.skills-grid span:hover {
  background: rgba(34, 211, 238, 0.2);
  transform: translateY(-2px);
  border-color: var(--accent-cyan);
}

.nav-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin-top: 8px;
}

.nav-item {
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 14px 18px;
  border: 1px solid var(--border-light);
  border-radius: 18px;
  background: rgba(0, 0, 0, 0.2);
  cursor: pointer;
  transition: all var(--transition-smooth);
  position: relative;
  overflow: hidden;
}

.nav-glow {
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 30% 50%, rgba(34, 211, 238, 0.15), transparent 70%);
  opacity: 0;
  transition: opacity var(--transition-smooth);
}

.nav-item:hover .nav-glow,
.nav-item.active .nav-glow {
  opacity: 1;
}

.nav-item:hover,
.nav-item.active {
  border-color: rgba(34, 211, 238, 0.6);
  background: rgba(34, 211, 238, 0.05);
  transform: translateX(4px);
}

.nav-number {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  color: var(--accent-cyan);
}

.nav-status {
  font-weight: 600;
  letter-spacing: 0.05em;
  font-size: 0.85rem;
  color: var(--text-primary);
}

.social-wrap {
  display: flex;
  gap: 18px;
  margin-top: 32px;
  padding-top: 20px;
  border-top: 1px solid var(--border-light);
}

.social-wrap a {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: var(--text-secondary);
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 500;
  transition: all var(--transition-fast);
  padding: 4px 8px;
  border-radius: 30px;
}

.social-wrap a:hover {
  color: var(--accent-cyan);
  transform: translateY(-2px);
  background: rgba(34, 211, 238, 0.1);
}

@media (max-width: 640px) {
  .profile-panel {
    position: relative;
    top: 0;
    padding: 20px;
  }

  .profile-head {
    flex-direction: column;
    text-align: center;
  }

  .meta-list p {
    width: 100%;
    justify-content: center;
  }

  .skills-grid {
    justify-content: center;
  }

  .social-wrap {
    justify-content: center;
    display: none;
  }
}
</style>