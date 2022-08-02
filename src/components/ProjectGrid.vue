<template>
  <div class="do-grid">
    <ProjectSingle
      v-for="project in projects"
      :key="project"
      :date="project.date"
      :status="project.status"
      :description="project.description"
      :video="project.video"
      :url="project.url"
      :framework="project.framework"
      :title="project.title"
    />
  </div>
</template>

<script>
import ProjectSingle from "./ProjectSingle.vue";
export default {
  components: {
    ProjectSingle,
  },

  data() {
    return {
      projects: [
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "VUE.JS ",
          title: "Cash App ",
          description: "Manage you cash",
          video: "Click here.....",
          url: "https://cashapphelp.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Hover Calendar",
          description: "Plan your day ahead!",
          url: "https://confident-swirles-c9499b.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "March 17, 2022",
          status: "Online",
         framework: "VUE.JS ",
          title: "Listing Resturant ",
          description: "Resturants around the world",
          url: "https://loving-shaw-867970.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "March 7 2022, ",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Infinite Dog App",
          description: "Infinite Dog App with images!",
          url: "https://infinitedogapp.netlify.app",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "December 22, 2021",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Dad's Joke ",
          description: "Random Daddy's Jokes !",
          url: "https://practical-mclean-b935e5.netlify.app",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "HTML & CSS",
          title: "Adeori Resturant",
          description: "Enjoy a nice meal at Adeori Resturant!",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "Click here",
          slides: "Slides",
        },
      ],
    };
  },
};
</script>

<style scoped>
.do-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 10px;
}

@media (max-width: 380px) {
.do-grid{
   display: grid;
  grid-template-columns:  1fr;
  grid-gap: 10px
}
}
</style>
