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
          framework: "JAVASCRIPT",
          title: "Currency Calculator",
          description: "Calculate world's currentcy ",
          video: "Click here.....",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Random Jokes",
          description: "Random jokes that will crack you up!",
          video: "Click here.....",
          url: "https://trusting-yalow-1c4467.netlify.app",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Quack Game",
          description: "Funny Quack game!",
          url: "https://compassionate-mestorf-c92499.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "Jan 25, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Live Clock",
          description: "Live clock",
          url: "https://friendly-fermat-83201f.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "VUE.JS",
          title: "Appruve Questionaire",
          description: "Appruve Questionaire",
          url: "https://musing-bell-11b20c.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "VUE.JS",
          title: "List Page",
          description: "Listing of world resturant",
          url: "https://loving-shaw-867970.netlify.app",
          video: "Click here.....",
          slides: "Slides",
        },
        {
          date: "July 22, 2022",
          status: "Online",
          framework: "JAVASCRIPT",
          title: "Calendar",
          description: "Plan your day ahead today!",
          url: "https://confident-swirles-c9499b.netlify.app",
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
  margin: -15px -15px;
}
.project-box {
  width: 320px;
  background: rgb(32, 32, 34);
  padding-left: 20px;
  padding-top: 40px;
  padding-bottom: 40px;
  padding-left: 40px;
  padding-right: 40px;
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
  font-size: 14px;
}
.framework p {
  letter-spacing: 5px;
  font-size: 14px;
  color: rgb(255, 255, 255);
}
.title h2 {
  line-height: 1.3;
  font-size: 24px;
  /* color: red; */
}
.main {
  padding-top: 30px;
}
.rating a {
  margin: 5px 10px;
  text-decoration: none;
  color: rgb(148, 148, 149);
  font-size: 14px;
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
@media (max-width: 480px) {
  .projects {
    line-height: 1;
  }

  .project-box {
    width: 330px;
    height: 28vh;
  }
  .rating a {
    font-size: 12px;
  }
  .project-box h2 {
    font-size: 16px;
  }
  .project-box h3 {
    font-size: 12px;
  }
  .project-box p {
    line-height: 1.5;
    font-size: 12px;
    width: 10em;
  }
  .lar {
    font-size: 16px;
  }
}
@media (max-width: 320px) {
  .projects {
    line-height: 1;
  }
  .project-box {
    width: 220px;
    height: 35vh;
  }
 
  .project-box h2 {
    font-size: 12px;
  }
  .project-box h3 {
    font-size: 12px;
  }
  .project-box p {
    line-height: 1.5;
    font-size: 12px;
    width: 10em;
  }
  .lar {
    font-size: 12px;
  
  }
   .rating{
 margin: -15px 0px;
   }
   .rating a {
    font-size: 12px;
   
  }
}
</style>
