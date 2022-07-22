<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <div class="app">
    <Profile class="profile" />
    <div class="project-work">
      <div class="project">
        <Projects />
        <div class="flex">
          <ProjectFlex />
          <ProjectGrid />
        </div>
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
}

:root {
  --clr-dark: 230 35% 7%;
  --clr-light: 231 77% 90%;
  --clr-white: 0 0% 100%;

  /* fonts-sizes */
  --fs-900: 9.075rem;
  --fs-800: 6.25rem;
  --fs-700: 3.5rem;
  --fs-600: 2.2rem;
  --fs-500: 1.75rem;
  --fs-400: 1.25rem;
  --fs-300: 1rem;
  --fs-200: 0.875rem;

  /* font-families */
  --ff-serif: "Bellefair", serif;
  --ff-sans-cond: "Barlow Condensed", sans-serif;
  --ff-sans-normal: "Barlow", sans-serif;
}
*,
:after,
:before {
  box-sizing: border-box;
  /* border: 0 solid #e5e7eb; */
}
/* Reset margins */

/* set up the body */
body {
  line-height: 1.5;
  font-size: var(--fs-400);
  color: rgb(255, 255, 255);
  background: rgb(21, 21, 21);
  font-family: "Inter var", sans-serif;
}
.app {
  display: flex;
  margin-left: auto;
  margin-right: auto;
  padding-left: 80px;
  /* padding-right: 80px; */
  /* position: fixed; */
}
.profile {
  /* width: 650px; */
}
.project-work {
  overflow-y: auto;
  height: 100vh;
  widows: 100%;
}
.project-work::-webkit-scrollbar {
  display: none;
}
.profile {
  overflow: ;
}
@media (max-width: 680px) {
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 10px;
    padding-right: 10px;
    overflow-x: hidden;
    display: block;
  }
}
.profile {
  padding-right: 100px;
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
