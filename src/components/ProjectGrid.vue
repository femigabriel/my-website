<template>
  <div class="project-flex">
    <div class="remote-project">
      <div class="project-box" v-for="project in projects" :key="project">
        <div class="status">
          <div class="framework">
            <p>{{ project.framework }}</p>
          </div>
          <div class="status">
            <p>{{ project.status }}</p>
          </div>
          <div class="date">
            <p>{{ project.date }}</p>
          </div>
        </div>
        <div class="title">
          <h2>{{ project.description }}</h2>
        </div>
        <div class="main flex">
          <div class="rating flex">
            <div class="icon"><i class="las la-external-link-alt"></i></div>

            <a target="_blank" :href="project.url">{{ project.video }}</a>
          </div>
          <div class="rating flex"></div>
        </div>
      </div>
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
          framework: "JAVASCRIPT",
          title: "Todo List",
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
          description: "Book your returant ahead anywhere in the world.",
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
.remote-project {
  display: flex;
  flex-direction: column;
  padding-top: 40px;
  margin: 15px -18px;
}
.project-box {
  /* width: 380px; */
  width: 320px;
  /* height: 50vh; */
  background: rgb(32, 32, 34);
  padding-left: 40px;
  padding-right: 40px;
  padding-top: 40px;
  padding-bottom: 40px;
  border-radius: 5px;
  margin: 5px 20px;
  cursor: pointer;
  line-height: 0.8;
}
.project-box:hover {
  /* width: 390; */
  /* height: 55vh; */
  box-shadow: 2px 9px 19px 15px #0000001f;
  transform: scale(1.1);
  -webkit-transition: all 200ms ease-in;
  -webkit-transform: scale(1.1);
  -ms-transition: all 200ms ease-in;
  -ms-transform: scale(1.1);
  -moz-transition: all 200ms ease-in;
  -moz-transform: scale(1.1);
  transition: all 200ms ease-in;
}
.status p {
  color: rgb(148, 148, 149);
  font-size: 14px;
}
/* .status h3 {
  letter-spacing: 3px;
  font-size: 1.7em;
} */
.framework p {
  letter-spacing: 5px;
  font-size: 14px;
  color: rgb(255, 255, 255);
}
.title {
  line-height: 1.2;
}
.title h2 {
  line-height: 1.3;
  font-size: 24px;
}
.main {
  padding-top: 30px;
}
.rating a {
  margin: 5px 15px;
  text-decoration: none;
  color: rgb(148, 148, 149);
  font-size: 14px;
}
.icon {
}
.las {
  color: rgb(148, 148, 149);
  font-size: 24px;
}
@media (max-width: 680px) {
  .project-box {
  }
  .title {
    width: 13em;
    font-size: 14px;
    line-height: 1;
  }
  .rating a {
    font-size: 14px;
    padding-bottom: 20px;
  }
}
</style>
