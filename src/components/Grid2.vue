<template>
  <div>
      <div class="gd">
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
    </div>
</template>

<script>
export default {
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
          framework: "VUE.JS ",
          title: "Listing Resturant",
          description: "Listing Resturant",
          url: "https://listingapp.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "March 17, 2022",
          status: "Online",
          framework: "VUE.JS ",
          title: "Digital Clock",
          description: "Digital Clock",
          url: "https://friendly-fermat-83201f.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "March 7 2022, ",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Currency Calculator",
          description: "World currency exchange calculator!",
          url: "https://confident-hawking-810c06.netlify.app/",
          video: "Click here",
          slides: "Slides",
        },
        {
          date: "December 22, 2021",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Whack Game ",
          description: "Whack a mole game",
          url: "https://compassionate-mestorf-c92499.netlify.app/",
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

}
</script>

<style>

</style>