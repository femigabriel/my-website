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
          framework: "React",
          date: "",
          status: "Online",
          title: "Orewa City",
          description: "",
          video: "Click here",
          url: "https://app.orewacity.com/",
          slides: "Slides",
        },
        {
          framework: "React",
          date: "",
          status: "Online",
          title: "Mualine",
          description: "Makeup & Hair Service Provider",
          video: "Click here",
          url: "https://mualine.ng/",
          slides: "Slides",
        },
        {
          framework: "REACT",
          date: "Feb, 2022",
          status: "Online",
          description:
            "Maildrip helps users to Send drip emails that reach the heart of your audience with Maildrip’s easy-to-use platform, guaranteed to improve sales.",
          title: "Maildrip ",
          video: "Click here",
          url: "https://app.maildrip.io/",
          slides: "Slides",
        },
        {
          framework: "React",
          date: "May, 2023",
          status: "Online",
          title: "Digital Story Book",
          description: "Online story book with games",
          video: "Click here",
          url: "https://book-app-nu.vercel.app/",
          slides: "Slides",
        },
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
          description:
            "Global healthcare delivery where users can pay for medications for loved ones anywhere around the world.",
          title: "Aluuka ",
          video: "Click here",
          url: "https://https://app.aluuka.io/",
          slides: "Slides",
        },
        {
          framework: "REACT",
          date: "Jan, 2022",
          status: "Online",
          title: "Adeori Car Rental App",
          description: "Car rental services app",
          video: "Click here",
          url: "https://adeori-cars.vercel.app/",
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
          url: "https://multi-step-form-self.vercel.app/",
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
          title: "Multi page Form",
          description: "Multi step Page form",
          video: "Click here",
          url: "https://multi-step-form-self.vercel.app/",
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
