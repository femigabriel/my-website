<template>
  <div class="do-grid">
    <div class="grid-1">
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
    <div>
      <div class="grid-2">
        <ProjectSingle
          v-for="project in grids"
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
    </div>
    <Grid2 />
  </div>
</template>

<script>
import ProjectSingle from "./ProjectSingle.vue";
import Grid2 from "./Grid2.vue";
export default {
  components: {
    ProjectSingle,
    Grid2,
  },

  data() {
    return {
      projects: [
        {
          date: "July 22, 2020",
          status: "Online",
          framework: "VUE.JS ",
          title: "Cash App ",
          description: "Manage you cash",
          video: "Click here.....",
          url: "https://cashapphelp.netlify.app",
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
          date: "July 22, 2020",
          status: "Online",
          framework: "VUE.JS ",
          title: "Listing Resturant",
          description: "Listing Resturant",
          url: "https://listingapp.netlify.app/",
          video: "Click here",
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
          date: "July 22, 2021",
          status: "Online",
          framework: "VUE.JS",
          title: "LocaHost Chat rooms",
          description: "Local Host Chat Rooms",
          video: "Click here",
          url: "https://localhostchatrooms.netlify.app/",
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
          date: " ",
          status: "Online",
          framework: "JS, HTML & CSS",
          title: "Image Galary ",
          description: "Flex Panel",
          url: "https://amazing-murdock-3e0b46.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },

        {
          date: "March 7 2020 ",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Currency Calculator",
          description: "World currency exchange calculator!",
          url: "https://confident-hawking-810c06.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "December 22, 2020",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Whack Game ",
          description: "Whack a mole game",
          url: "https://compassionate-mestorf-c92499.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "July 22, 2020",
          status: "Online",
          framework: "HTML & CSS",
          title: "Adeori Resturant",
          description: "Enjoy a nice meal at Adeori Resturant!",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "Click here",
          slides: "Slides",
        },
      ],
      grids: [
        {
          date: "July 22, 2020",
          status: "Online",
          framework: "JS, HTML & CSS",
          title: "Friends Zone",
          description: "Search for all my friends",
          url: "https://myfriendszone.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "",
          status: "Online",
          framework: "HTML & CSS",
          title: "Adeori Resturant",
          description: "Enjoy a nice meal at Adeori Resturant!",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: " ",
          status: "Online",
          framework: "JS, HTML & CSS",
          title: "Live Calendar ",
          description: "Live calendar",
          url: "https://upbeat-snyder-aa1648.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "March 17, 2020",
          status: "Online",
          framework: "VUE.JS ",
          title: "Digital Clock",
          description: "Digital Clock",
          url: "https://friendly-fermat-83201f.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: " ",
          status: "Online",
          framework: "JS, HTML & CSS",
          title: "Image Galary ",
          description: "Flex Panel",
          url: "https://amazing-murdock-3e0b46.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "",
          status: "Online",
          framework: "JAVASCRIPT ",
          title: "Calculator ",
          description: "Calculator ",
          url: "https://affectionate-stonebraker-f201de.netlify.app/",
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
  padding-top: 60px;
}
.grid-1 {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 10px;
}
.grid-2 {
  display: grid;
  grid-template-columns: 1fr;
  grid-gap: 10px;
  margin-top: 40px;
}

@media (max-width: 420px) {
  .do-grid {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 10px;
  }
}
</style>
