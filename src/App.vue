<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <div class="app">
    <Profile :activeId="current" @setActivePage="setActivePage" class="profile" />
    <div class="current">
      <div class="project-work">
        <div
          class="projects"
          v-show="current == 0"
        >
          <Projects />
          <div class="project-flex">
            <ProjectFlex />
            <ProjectGrid />
          </div>
        </div>
        <div v-show="current == 1">
          <Resume class="resume" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Profile from "./components/Profile.vue";
import Projects from "./components/Projects.vue";
import ProjectFlex from "./components/ProjectFlex.vue";
import ProjectGrid from "./components/ProjectGrid.vue";
import Resume from "./components/Resume.vue";
export default {
  name: "App",
  components: {
    Profile,
    Projects,
    ProjectFlex,
    ProjectGrid,
    Resume,
  },
  data() {
    return {
      current: 1,
    };
  },
  methods:{
    setActivePage(value){
      this.current=value
    }
  }
};
</script>

<style>
@import url("https://rsms.me/inter/inter.css");
#app {
  margin-top: 60px;
  width: 100%;
  /* flex-shrink: 0; */
}

*,
:after,
:before {
  box-sizing: border-box;
   
}
body {
  line-height: 1;
  color: rgb(255, 255, 255);
  background: rgb(21, 21, 21);
  font-family: "Inter var", sans-serif;
  width: 100%;
}

.app {
  display: flex;
  margin-left: auto;
  margin-right: auto;
  padding-left: 80px;
  padding-right: 80px;
  position: fixed;
}
.current {
  display: block;
}
.profile {
  padding-right: 80px;
}
.project-work {
  /* display: none; */
  overflow-y: auto;
  max-height: 100vh;
}
.resume {
  /* display: ; */
}
.project-work::-webkit-scrollbar {
  /* display: none; */
}

.projects {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding-right: 20px;
}

.project-flex {
  /* display: none; */
  display: flex;
  width: 600px;
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
}
.flex {
  display: flex;
}
span {
  color: rgb(148, 148, 149);
}

.grid {
  display: flex;
  margin: 10px 15px;
}
@media (min-width: 45rem) {
}
</style>
