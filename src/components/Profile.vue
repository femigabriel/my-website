<template>
  <aside class="profile-page">
    <div>
      <div class="profile-head">
        <img src="../images/LIN.jpg" alt="Ogungbade Femi" />
        <div>
          <h1>Ogungbade Femi</h1>
          <p>Frontend Developer</p>
        </div>
      </div>

      <p class="about">
        I build clean, high-performing web products with Vue and React. I care
        about thoughtful UI structure, smooth interaction, and mobile-first
        delivery.
      </p>

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
        href="https://www.linkedin.com/in/ogungbade-oluwafemi-25b28619a/"
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

.profile-head {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 20px;
}

.profile-head img {
  width: 72px;
  height: 72px;
  border-radius: 18px;
  object-fit: cover;
  border: 1px solid rgba(148, 163, 184, 0.35);
}

.profile-head h1 {
  font-size: 1.4rem;
  line-height: 1.2;
}

.profile-head p {
  color: #22d3ee;
  margin-top: 4px;
  font-size: 0.92rem;
}

.about {
  color: #94a3b8;
  line-height: 1.7;
  margin-bottom: 28px;
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
