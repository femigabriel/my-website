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
        <transition name="fade" mode="out-in">
          <!-- Wrap both sections in a single div or use component :is -->
          <div key="content">
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
          </div>
        </transition>

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
          title: "Digital Book App",
          framework: "EdTech Platform",
          status: "Live",
          date: "2026",
          description:
            "Three Paths Ile Social Emotion Learning platform with a unique blend of reading and activities, inspired by Charlie's Big Gift.",
          highlight: "Education",
          url: "https://digital-book-app.vercel.app/",
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
          title: "Speech Help",
          framework: "Assistive Communication App",
          status: "Live",
          date: "2026",
          description:
            "Speech support platform focused on guided communication workflows. Demo access requires account login.",
          highlight: "Accessible Tech",
          url: "https://speech-help.vercel.app/",
          cta: "Visit project",
        },
        {
          title: "HomeSummo",
          framework: "Property Platform",
          status: "Client Host",
          date: "2026",
          description:
            "Real estate experience deployed on client infrastructure. Availability may vary depending on host billing status.",
          highlight: "Client Delivery",
          url: "https://www.homesummo.com/",
          cta: "Visit project",
        },
        {
          title: "LawTabby",
          framework: "Legal Tech Platform",
          status: "Live",
          date: "2026",
          description:
            "Legal workflow product with user onboarding and Google Single Sign-On authentication.",
          highlight: "Legal Tech",
          url: "https://lawtabby.onrender.com/",
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
          title: "Pathspring",
          framework: "Frontend Engineering",
          status: "Live",
          date: "2026",
          description:
            "The reading platform for every reader. Whether you're a school looking to transform reading instruction or a family wanting to nurture a love of reading, PathSpring has you covered.",
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
@import url("https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap");

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --bg-dark: #0a0a0f;
  --bg-panel: rgba(18, 22, 35, 0.75);
  --border-light: rgba(148, 163, 184, 0.15);
  --text-primary: #f1f5f9;
  --text-secondary: #94a3b8;
  --accent-cyan: #22d3ee;
  --accent-blue: #38bdf8;
  --glow-cyan: rgba(34, 211, 238, 0.2);
  --card-bg: rgba(30, 35, 50, 0.5);
  --transition-fast: 0.2s ease;
  --transition-smooth: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

html,
body,
#app {
  min-height: 100%;
  scroll-behavior: smooth;
}

body {
  font-family: "Inter", sans-serif;
  background-color: var(--bg-dark);
  color: var(--text-primary);
  background-image: 
    radial-gradient(circle at 10% 20%, rgba(34, 211, 238, 0.08) 0%, transparent 50%),
    radial-gradient(circle at 90% 70%, rgba(56, 189, 248, 0.06) 0%, transparent 55%);
  background-attachment: fixed;
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
    linear-gradient(135deg, rgba(34, 211, 238, 0.05) 0%, transparent 40%),
    linear-gradient(225deg, rgba(56, 189, 248, 0.05) 0%, transparent 45%);
  z-index: 0;
}

.app-layout {
  position: relative;
  z-index: 1;
  max-width: 1400px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 340px 1fr;
  gap: 28px;
}

.main-panel {
  background: var(--bg-panel);
  backdrop-filter: blur(16px);
  border: 1px solid var(--border-light);
  border-radius: 28px;
  padding: 36px;
  transition: all var(--transition-smooth);
}

.section-header {
  margin-bottom: 32px;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.12em;
  color: var(--accent-cyan);
  font-size: 0.75rem;
  font-weight: 600;
  margin-bottom: 12px;
}

.section-header h2 {
  font-size: clamp(1.8rem, 3vw, 2.6rem);
  font-weight: 700;
  letter-spacing: -0.02em;
  margin-bottom: 14px;
  background: linear-gradient(135deg, #fff, var(--accent-blue));
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
}

.section-header p {
  color: var(--text-secondary);
  max-width: 680px;
  line-height: 1.6;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s ease, transform 0.25s ease;
}

.fade-enter-from {
  opacity: 0;
  transform: translateY(8px);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}

.socials-footer {
  display: none;
}

@media (max-width: 1080px) {
  .app-layout {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .main-panel {
    padding: 28px;
  }
}

@media (max-width: 640px) {
  .app-shell {
    padding: 16px;
  }

  .main-panel {
    padding: 20px;
  }

  .socials-footer {
    display: block;
    margin-top: 28px;
  }
}
</style>