<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <div class="app-shell">
    <div class="bg-gradient"></div>
    <div class="app-layout">
      <Profile
        :activeId="current"
        @setActivePage="setActivePage"
        class="profile-panel"
      />

      <main class="main-panel">
        <section v-show="current === 0" class="projects-page">
          <header class="section-header">
            <p class="eyebrow">Portfolio</p>
            <h2>Selected Work</h2>
            <p>
              Production-ready applications across AI, HR, media, healthcare,
              and workflow automation.
            </p>
          </header>

          <ProjectFlex :projects="featuredProjects" />
          <ProjectGrid :projects="remainingProjects" />
        </section>

        <section v-show="current === 1" class="resume-page">
          <Resume :projects="projects" />
        </section>

        <SocialFooter class="socials-footer" />
      </main>
    </div>
  </div>
</template>

<script>
import Profile from "./components/Profile.vue";
import ProjectFlex from "./components/ProjectFlex.vue";
import ProjectGrid from "./components/ProjectGrid.vue";
import Resume from "./components/Resume.vue";
import SocialFooter from "./components/SocialFooter.vue";

export default {
  name: "App",
  components: {
    Profile,
    ProjectFlex,
    ProjectGrid,
    Resume,
    SocialFooter,
  },
  data() {
    return {
      current: 0,
      projects: [
        {
          title: "EventHub",
          framework: "Vue, Product Platform",
          status: "Live",
          date: "2026",
          description:
            "The all-in-one platform for creating, managing, and scaling events. Built for workshops through large conferences.",
          highlight: "Latest Build",
          url: "https://event-hub-three-red.vercel.app/",
          cta: "Visit project",
        },
        {
          title: "Curation AI",
          framework: "AI Workflow App",
          status: "Live",
          date: "2026",
          description:
            "Curation AI authenticates digital content and analyzes real public sentiment before organizations make critical decisions.",
          highlight: "AI Product",
          url: "https://www.curationai.ai/",
          cta: "Visit project",
        },
        {
          title: "Maildrip",
          framework: "Email Automation Platform",
          status: "Live",
          date: "2025",
          description:
            "Developed responsive frontend workflows and optimized campaign creation experiences for modern email marketing automation.",
          highlight: "SaaS Product",
          url: "https://app.maildrip.io/",
          cta: "Visit project",
        },
        {
          title: "Almedin",
          framework: "HR Management System",
          status: "Live",
          date: "2025",
          description:
            "Built dashboard interfaces and integrated APIs to support employee management, operations visibility, and workflow execution.",
          highlight: "HR Tech",
          url: "https://almedin-project.vercel.app/",
          cta: "Visit project",
        },
        {
          title: "Aluuka",
          framework: "Healthcare Platform",
          status: "Live",
          date: "2025",
          description:
            "Implemented accessible service flows and clean UI architecture to improve healthcare navigation and service booking.",
          highlight: "HealthTech",
          url: "https://aluuka.io/",
          cta: "Visit project",
        },
        {
          title: "Hellyes Media",
          framework: "Marketing Platform",
          status: "Live",
          date: "2026",
          description:
            "A conversion-focused digital media experience with clear messaging, polished interactions, and modern visual hierarchy.",
          highlight: "Brand Experience",
          url: "https://aihellyesmedia.com/",
          cta: "Visit project",
        },
        {
          title: "WorkPadi",
          framework: "Web App",
          status: "Live",
          date: "2026",
          description:
            "The modern HR platform built for teams that want to work smarter. Automate compliance, engage your workforce, and make data-driven decisions with WorkPadi's all-in-one solution.",
          highlight: "Collaboration",
          url: "https://work-padi.vercel.app/",
          cta: "Visit project",
        },
        {
          title: "Complaint Fix",
          framework: "AI Application",
          status: "Live",
          date: "2026",
          description:
            "A simple AI application that handles responses with a deep understanding of customer needs, delivering swift and accurate solutions while maintaining empathy and adherence to company policies and complaint regulatory guides.",
          highlight: "Support AI",
          url: "https://complaintgpt.vercel.app/",
          cta: "Visit project",
        },
        {
          title: "Pathspring Frontend",
          framework: "Frontend Engineering",
          status: "Live",
          date: "2026",
          description:
            "Modern frontend implementation centered on clean component structure, scalability, and polished UX details.",
          highlight: "Frontend",
          url: "https://pathspring-frontend.vercel.app/",
          cta: "Visit project",
        },
      ],
    };
  },
  computed: {
    featuredProjects() {
      return this.projects.slice(0, 2);
    },
    remainingProjects() {
      return this.projects.slice(2);
    },
  },
  methods: {
    setActivePage(value) {
      this.current = value;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --bg: #05070d;
  --panel: rgba(15, 23, 42, 0.82);
  --panel-border: rgba(148, 163, 184, 0.22);
  --text: #e2e8f0;
  --muted: #94a3b8;
  --accent: #22d3ee;
  --accent-strong: #38bdf8;
}

html,
body,
#app {
  min-height: 100%;
}

body {
  color: var(--text);
  background:
    radial-gradient(circle at 15% 20%, rgba(34, 211, 238, 0.16), transparent 38%),
    radial-gradient(circle at 80% 0%, rgba(56, 189, 248, 0.2), transparent 42%),
    var(--bg);
  font-family: "Space Grotesk", sans-serif;
}

a {
  color: inherit;
}

.app-shell {
  position: relative;
  width: 100%;
  min-height: 100vh;
  padding: 28px;
}

.bg-gradient {
  position: fixed;
  inset: 0;
  pointer-events: none;
  background:
    linear-gradient(125deg, rgba(34, 211, 238, 0.08), transparent 35%),
    linear-gradient(320deg, rgba(56, 189, 248, 0.08), transparent 45%);
}

.app-layout {
  position: relative;
  z-index: 1;
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 320px 1fr;
  gap: 24px;
}

.profile-panel,
.main-panel {
  background: var(--panel);
  border: 1px solid var(--panel-border);
  backdrop-filter: blur(12px);
  border-radius: 22px;
}

.main-panel {
  padding: 34px;
}

.section-header {
  margin-bottom: 24px;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.14em;
  color: var(--accent);
  font-size: 12px;
  margin-bottom: 10px;
}

.section-header h2 {
  font-size: clamp(1.8rem, 2.8vw, 2.4rem);
  margin-bottom: 12px;
}

.section-header p {
  color: var(--muted);
  max-width: 680px;
  line-height: 1.7;
}

.socials-footer {
  display: none;
}

@media (max-width: 1080px) {
  .app-layout {
    grid-template-columns: 1fr;
  }

  .main-panel {
    padding: 26px;
  }
}

@media (max-width: 640px) {
  .app-shell {
    padding: 12px;
  }

  .main-panel {
    padding: 18px;
  }

  .section-header {
    margin-bottom: 18px;
  }

  .socials-footer {
    display: block;
    margin-top: 18px;
  }
}
</style>
