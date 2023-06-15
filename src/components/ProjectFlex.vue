<template>
  <div class="single-item" v-for="project in projects" :key="project">
    <ProjectSingle
      :description="project.description"
      :video="project.video"
      :url="project.url"
      :isRectangle="true"
      :framework="project.framework"
      :title="project.title"
    />
  </div>
</template>

<script>
import ProjectSingle from "./ProjectSingle.vue";
export default {
  data() {
    return {
      projects: [
        {
          framework: "REACT TYPESCRIPT",
          date: "Dec, 2021",
          status: "Online",
          title: "Musica App",
          description: "Latest Naija R & B Hits",
          video: "Click here",
          url: "https://musicamusic.netlify.app/",
          slides: "Slides",
        },
        {
          framework: "REACT",
          date: "Feb, 2022",
          status: "Online",
          description: "Maildrip helps users to Send drip emails that reach the heart of your audience with Maildrip’s easy-to-use platform, guaranteed to improve sales.",
          title: "Maildrip ",
          video: "Click here",
          url: "https://https://app.maildrip.io/",
          slides: "Slides",
        },
        {
          framework: "REACT TYPESCRIPT",
          date: "Nov, 2021",
          status: "Online",
          title: "Multi-Step Game",
          description: "Multi step game form",
          video: "Click here",
          url: "https://multistepformgame.netlify.app/",
          slides: "Slides",
        },
        {
          framework: "REACT.JS",
          date: "August 29, 2022",
          status: "Online",
          title: "Crappo Crypto Exchange App",
          description: "Free Cryptocurrency App",
          video: "Click here",
          url: "https://crappocryptocurrency.netlify.app/",
          slides: "Slides",
        },
        {
          date: "July 22, 2021",
          status: "Online",
          framework: "VUE.JS",
          title: "JUNGIAN ARCHETYPE QUIZ",
          description:
            "Free Archetype Quiz Reveals Your Personality Quirks, Innate Talents, and Hidden Weaknesses!",
          video: "Click here",
          url: "https://archytype-quiz.netlify.app/",
          slides: "Slides",
        },

        {
          framework: "NEXT.JS",
          date: "August 29, 2021",
          status: "Online",
          title: "Crappo App Landing Page",
          description: "Free Cryptocurrency App",
          video: "Click here",
          url: "https://crappocoin-app.netlify.app/",
          slides: "Slides",
        },

        {
          framework: "REACT.JS",
          date: "Dec, 2021",
          status: "Online",
          title: "Emploment Screening Dashboard",
          description: "creening Dashboard",
          video: "Click here",
          url: "https://employment-dasboard.netlify.app/",
          slides: "Slides",
        },

        {
          framework: "NEXT.JS",
          date: "August 22, 2021",
          status: "Online",
          title: "Deallus App",
          description: "Church Development app",
          video: "Click here",
          url: "https://deallus-app.netlify.app/",
          slides: "Slides",
        },
        {
          framework: "REACT JS",
          date: "August 12, 2021",
          status: "Online",
          title: "Simple Maths Game",
          description: "Simple Maths Game",
          video: "Click here",
          url: "https://easymathgame.netlify.app/",
          slides: "Slides",
        },

        {
          framework: "VUE.JS",
          date: "July 22, 2021",
          status: "Online",
          title: "API Dog App",
          description: "Random Dog App with images",
          video: "Click here",
          url: "https://infinitedogapp.netlify.app",
          slides: "Slides",
        },

        {
          date: "July 22, 2021",
          status: "Online",
          framework: "VUE.JS",
          title: "LocaHost Chat rooms",
          description: "Local Host Chat Rooms",
          video: "Click here",
          url: "https://localhostchatrooms.netlify.app/",
          slides: "Slides",
        },
      ],
    };
  },
  components: { ProjectSingle },
};
</script>

<style scoped>
.single-item {
  margin-bottom: 10px;
}
@media (max-width: 380px) {
  .single-item {
    margin-top: 10px;
  }
}
</style>
