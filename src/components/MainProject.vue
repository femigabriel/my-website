<template>
  <div class="main">
    <div class="content-box" v-for="project in projects" :key="project">
      <p>{{ project.framework }}</p>
      <h2>{{ project.title }}</h2>
      <div class="description">
        <p>{{ project.description }}</p>
      </div>

      <div class="rating flex">
        <div class="icon"><i class="lar la-star"></i></div>
        <a target="_blank" :href="project.url">{{ project.video }}</a>
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
          video: "Click here.....",
        },
        {
          framework: "JAVASCRIPT",
          title: "Todo List",
          description: "Plan your day ahead!",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "Click here.....",
        },
        {
          framework: "VUE.JS",
          title: "Mum's Cake",
          description: "Cake store for all sorts of cakes",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "Click here.....",
        },
        {
          framework: "VUE.JS",
          title: "Dad's Joke",
          description: "Every funny daddy's jokes ",
          url: "hhttps://laughing-dubinsky-710f9c.netlify.app",
          video: "Click here.....",
        },
      ],
    };
  },
};
</script>

<style scoped>
.projects {
  line-height: 1;
  width: 100%;
  overflow-x: hidden;
}
.content {
  margin: 10px 10px;
}
.project-box {
  max-width:648px;
  /* width: 648px; */
  /* height: 33vh; */
  background: rgb(32, 32, 34);
  padding-left: 60px;
  padding-right: 40px;
  padding-bottom: 20px;
  padding-top: 20px;
  border-radius: 5px;
  margin-bottom: 10px;
  cursor: pointer;
}
.project-box:hover {
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

.project-box p {
  text-transform: capitalize;
  font-size: 14px;
  font-weight: 600;
  letter-spacing: 3px;
}
.description p {
  font-size: 14px;
  color: rgb(148, 148, 149);
  letter-spacing: normal;
}
.rating a {
  margin: 5px 10px;
  text-decoration: none;
  color: rgb(148, 148, 149);
  font-size: 14px;
}
.rating {
  /* margin: 20px 10px; */
  color: rgb(148, 148, 149);
}
.rating p {
  margin: 0px 15px;
}

.lar {
  font-size: 20px;
  color: rgb(148, 148, 149);
}
</style>
