<template>
  <div class="project-flex">
    <div class="remote-project">
      <div class="project-box" v-for="project in projects" :key="project">
        <div class="status">
          <h3>{{ project.framework }}</h3>
          <p>{{ project.status }}</p>
          <p>{{ project.date }}</p>
        </div>
        <div class="title">
          <h2>{{ project.description }}</h2>
        </div>
        <div class="main flex">
          <div class="rating flex">
            <div class="icon"><i class="las la-external-link-alt"></i></div>
            <a target="_blank" :href="project.url">{{ project.video }}</a>
          </div>

          <div class="rating flex">
            <!-- <div class="icon"><i class="las la-external-link-alt"></i></div>
            <p>{{ project.slides }}</p> -->
          </div>
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
          framework: "Javascript",
          title: "Currency Calculator",
          description: "Calculate world's currentcy ",
          video: "CLick here.....",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "Javascript",
          title: "Random Jokes",
          description: "Random jokes that will crack you up!",
          video: "CLick here.....",
          url: "https://trusting-yalow-1c4467.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "Javascript",
          title: "Quack Game",
          description: "Funny Quack game!",
          url: "https://compassionate-mestorf-c92499.netlify.app",
          video: "CLick here.....",
          slides: "Slides",
        },
        {
          date: "Jan 25, 2022",
          status: "Online",
          framework: "Javascript",
          title: "Live Clock",
          description: "Live clock",
          url: "https://friendly-fermat-83201f.netlify.app",
          video: "CLick here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "Vue.js",
          title: "Appruve Questionaire",
          description: "Appruve Questionaire",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "CLick here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Paris-France",
          framework: "Javascript",
          title: "Todo List",
          description: "Plan your day ahead today!",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "CLick here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Paris-France",
          framework: "Javascript",
          title: "Todo List",
          description: "Plan your day ahead today!",
          url: "https://nostalgic-lovelace-acc728.netlify.app",
          video: "CLick here.....",
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
  margin: -15px -15px;
}
.project-box {
  /* width: 380px;
  height: 50vh; */
  width: 275px;
  background: rgb(32, 32, 34);
  padding-left: 20px;
  /* padding-right: 40px; */
  padding-top: 30px;
  padding-bottom: 10px;
  border-radius: 5px;
  margin: 5px 23px;
  cursor: pointer;
  line-height: 0.8;
  transition: all 0.2s ease-in-out;
}
.project-box:hover {
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
}
.title {
  /* padding-top: 30px;
  font-size: var(--fs-500); */
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
}
.main p {
  font-size: 18px;
}
@media (max-width: 680px) {
   .title {
  width: 13em;
  font-size: 14px;
}
.rating a {
  font-size: 14px;
    padding-bottom: 10px;
}
}
</style>
