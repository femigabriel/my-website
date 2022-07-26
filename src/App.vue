<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <div class="app">
    <Profile class="profile" />

      <div class="projects">
        <Projects />
        <div class="project-flex">
          <ProjectFlex />
          <ProjectGrid />
      </div>
    </div>
  </div>
  <div class="grid"></div>
</template>

<script>
import Profile from "./components/Profile.vue";
import Projects from "./components/Projects.vue";
import ProjectFlex from "./components/ProjectFlex.vue";
import ProjectGrid from "./components/ProjectGrid.vue";
export default {
  name: "App",
  components: {
    Profile,
    Projects,
    ProjectFlex,
    ProjectGrid,
  },
};
</script>

<style>
@import url("https://rsms.me/inter/inter.css");
#app {
  margin-top: 60px;
  width: 100%;
  flex-shrink: 0;
}

*,
:after,
:before {
  box-sizing: border-box;
  /* border: 0 solid #e5e7eb; */
}
body {
  line-height: 1;
  color: rgb(255, 255, 255);
  background: rgb(21, 21, 21);
  font-family: "Inter var", sans-serif;
  width: 100%;
}
#app {
}
.app {
  display: flex;
  /* flex-shrink: 0; */
  margin-left: auto;
  margin-right: auto;
  padding-left: 60px;
  padding-right: 80px;
  /* position: fixed; */
}
.profile {
  /* width: 35%; */
  padding-right: 80px;
}
.project-work {
  /* overflow-y: auto; */
 
}
.project-work::-webkit-scrollbar {
  display: none;
}
.projects {
  display: flex;
  flex-direction: column;
   /* height: 100vh; */
  width: 100%;
  padding-right: 20px; 
  margin: 0px -30px;
   /* padding-left: 60px; */
}

.project-flex {
  display: flex;
  /* flex-shrink: 0; */
  width: 600px;
    /* padding-left: 60px; */
}
@media (max-width: 680px) {
  body {
    overflow-x: hidden;
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 15px;
    padding-right: 15px;
    overflow-x: hidden;
    display: block;
  }
  .projects {
    display: block;
  }
}
.profile {
  /* padding-right: 100px; */
}
.flex {
  display: flex;
}
span {
  color: rgb(148, 148, 149);
}

.grid {
  display: flex;
  /* justify-content: space-between; */
  margin: 10px 15px;
}
@media (min-width: 45rem) {
}
</style>
