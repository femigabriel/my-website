<template>
  <div class="projects">
    <div class="content">
      <div class="project-box" v-for="project in projects" :key="project">
        <h3>{{ project.framework }}</h3>
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
        <div class="rating flex">
          <div class="icon"><i class="lar la-star"></i></div>
          <a target="_blank" :href="project.url">{{ project.video }}</a>
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
          framework: "VUE.JS",
          title: "Dad's Joke",
          description: "Every funny daddy's jokes ",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "CLick here.....",
        },
        {
          framework: "JAVASCRIPT",
          title: "Todo List",
          description: "Plan your day ahead!",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "CLick here.....",
        },
        {
          framework: "VUE.JS",
          title: "Mum's Cake",
          description:
            "Cake store house where you can can buy all sorts of cakes ",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "CLick here.....",
        },
        {
          framework: "VUE.JS",
          title: "Dad's Joke",
          description: "Every funny daddy's jokes ",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "CLick here.....",
        },
      ],
    };
  },
};
</script>

<style scoped>
.projects {
  line-height: 1;
}
.content {
  margin: 10px 10px;
}
.project-box {
  width: 570px;
  height: 33vh;
  background: rgb(32, 32, 34);
  padding-left: 60px;
  padding-right: 40px;
  padding-top: 20px;
  border-radius: 5px;
  margin-bottom: 10px;
  cursor: pointer;
}
.project-box:hover {
  /* width: 790px; */
  height: 30vh;
  transform: scale(1.3);
  box-shadow: 2px 9px 19px 15px #0000001f;
  -webkit-transition: all 200ms ease-in;
  -webkit-transform: scale(1.1);
  -ms-transition: all 200ms ease-in;
  -ms-transform: scale(1.1);
  -moz-transition: all 200ms ease-in;
  -moz-transform: scale(1.1);
  transition: all 200ms ease-in;
}
.project-box h2 {
  font-size: 28px;
}
.project-box h3 {
  text-transform: capitalize;
  font-size: 16px;
  font-weight: 600;
}
.project-box p {
  font-size: 18px;
  color: rgb(148, 148, 149);
}
.rating a {
  margin: 5px 10px;
  text-decoration: none;
  color: rgb(148, 148, 149);
  font-size: 18px;
}
.rating {
  /* margin: 20px 10px; */
  color: rgb(148, 148, 149);
}
.rating p {
  margin: 0px 15px;
}
.icon {
}
.lar {
  /* margin: 0px 10px; */
  font-size: 24px;
  color: rgb(148, 148, 149);
}
@media (max-width: 680px) {
  .projects {
    line-height: 0.5;
  }
  .content {
  /* margin: 20px 30px; */
}
.project-box{

}
  .rating a {
    font-size: 14px;
  }
  .project-box h2 {
    font-size: 24px;
  }
  .project-box h3 {
    font-size: 14px;
  }
  .project-box p {
    font-size: 14px;
    line-height: 1.1;
  }
}
</style>
