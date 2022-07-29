<template>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/line-awesome/1.3.0/line-awesome/css/line-awesome.min.css"
  />
  <div class="app">
    <Profile
      :activeId="current"
      @setActivePage="setActivePage"
      class="profile"
    />
    <div class="current">
      <div class="project-work">
        <div class="projects" v-show="current == 0">
          <Projects />
          <div class="project-flex">
            <ProjectFlex />
            <ProjectGrid />
          </div>
        </div>
        <div v-show="current == 1">
          <Resume class="resume" />
        </div>
        <SocialFooter class="socials-footer" />
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
import SocialFooter from "./components/SocialFooter.vue";
export default {
  name: "App",
  components: {
    Profile,
    Projects,
    ProjectFlex,
    ProjectGrid,
    Resume,
    SocialFooter,
  },
  data() {
    return {
      current: 0,
    };
  },
  methods: {
    setActivePage(value) {
      this.current = value;
    },
  },
};
</script>

<style>
@import url("https://rsms.me/inter/inter.css");
#app {
  margin-top: 60px;
  width: 100%;
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
  /* overflow-y: auto; */
  /* max-height: 100vh; */
}
.current {
  display: block;
}
.profile {
  padding-right: 80px;
}
.project-work {
  overflow-y: auto;
  /* max-height: 100vh; */
}

.projects {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding-right: 20px;
}

.project-flex {
  display: flex;
  /* width: 600px; */
}
.resume {
  /* position: fixed; */
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
.socials-footer {
  display: block;
}
@media (max-width: 820px) {
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 60px;
    padding-right: 40px;
    overflow-x: hidden;
    display: block;
    /* max-height: 100vh; */
    position: static;
  }
  .projects {
    display: flex;
  }
  .project-flex {
    display: flex;
  }
}

@media (max-width: 480px) {
  body {
    overflow-x: hidden;
  }
  #app {
    margin-top: 40px;
    width: 100%;
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 25px;
    padding-right: 25px;
    overflow-x: hidden;
    display: block;
    /* max-height: 100vh; */
    position: static;
  }
  .projects {
    display: block;
  }
  .project-flex {
    display: block;
  }
  .project-work {
    overflow-y: auto;
    max-height: 100vh;
  }
}
@media (max-width: 380px) {
  body {
    overflow-x: hidden;
  }
  #app {
    margin-top: 20px;
    width: 100%;
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 15px;
    padding-right: 15px;
    overflow-x: hidden;
    display: block;
    /* overflow-y: auto; */
    /* max-height: 100vh; */
    position: static;
  }
  .projects {
    display: block;
  }
  .project-flex {
    display: block;
  }
  .project-work {
    overflow-y: auto;
    max-height: 100vh;
  }
  .socials-footer {
    display: block;
    /* position: fixed; */
  }
}
@media (max-width: 320px) {
  body {
    overflow-x: hidden;
  }
  #app {
    margin-top: 20px;
    /* width: 100%; */
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 15px;
    padding-right: 15px;
    overflow-x: hidden;
    display: block;
    /* max-height: 100vh; */
    position: static;
  }
  .projects {
    display: block;
  }
  .project-work {
    /* overflow-y: auto; 
     max-height: 100vh; */
  }
  .project-flex {
    display: block;
  }
  .socials-footer {
    display: block;
  }
}

@media (max-width: 280px) {
  body {
    overflow-x: hidden;
  }
  #app {
    margin-top: 20px;
    width: 100%;
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 20px;
    padding-right: 10px;
    overflow-x: hidden;
    display: block;
    overflow-y: auto;
    /* max-height: 100vh; */
    position: static;
  }
  .projects {
    display: block;
  }
  /* .project-work {
    overflow: hidden;
    max-height: 100vh;
  } */
  .project-work {
    /* overflow-y: auto;
    max-height: 100vh; */
  }
  .project-flex {
    display: block;
  }
  .socials-footer {
    display: block;
  }
}
</style>
