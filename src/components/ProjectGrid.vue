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
          framework: "VUE.JS",
          title: "Adeori Resturant",
          description: "Plan your day ahead!",
          url: "https://loving-shaw-867970.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "March 17, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Listing Resturant ",
          description: "Resturants around the world",
          url: "https://loving-shaw-867970.netlify.app/",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "March 7 2022, ",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Infinite Dog App",
          description: "Infinite Dog App with images!",
          url: "https://infinitedogapp.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "December 22, 2021",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Dad's Joke ",
          description: "Random Daddy's Jokes !",
          url: "https://practical-mclean-b935e5.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "HTML & CSS",
          title: "Adeori Resturant",
          description: "Enjoy a nice meal at Adeori Resturant!",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "Click here.....",
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
.title h2 {
  line-height: 1.3;
  font-size: 28px;
  margin: 40px 0px;
  color: red;
}
.title p {
  color: rgb(148, 148, 149);
  font-size: 18px;
}
.main {
  padding-top: 30px;
}
.rating a {
  margin: 5px 10px;
  text-decoration: none;
  color: rgb(148, 148, 149);
  font-size: 18px;
  padding-bottom: 20px;
}
.icon {
}
.las {
  /* margin: 0px 10px; */
  color: rgb(148, 148, 149);
  font-size: 24px;
  margin: 8px 2px;
}
.main p {
  font-size: 18px;
}
</style>
