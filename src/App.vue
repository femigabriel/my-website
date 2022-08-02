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
          <!-- <Projects /> -->
          <div class="project-flex">
            <div class="project-flex-class"><ProjectFlex /></div>
            <ProjectGrid />
          </div>
        </div>
        <div v-show="current == 1">
          <Resume class="resume" />
        </div>
        <SocialFooter class="socials-footer" />
      </div>
      <!-- <MainProject /> -->
    </div>
  </div>
</template>

<script>
import Profile from "./components/Profile.vue";
import ProjectFlex from "./components/ProjectFlex.vue";
import ProjectGrid from "./components/ProjectGrid.vue";
import Resume from "./components/Resume.vue";
import SocialFooter from "./components/SocialFooter.vue";

export default {
  name: "App",
  components: {
    Profile,
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

*,
:after,
:before {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  line-height: 1;
  color: rgb(255, 255, 255);
  background: rgb(21, 21, 21);
  font-family: "Inter var", sans-serif;
  width: 100%;
}

.project-flex-class {
  margin-bottom: 10px;
}

.app {
  display: flex;
  margin-left: auto;
  margin-right: auto;
  padding-top: 120px;
  padding-left: 80px;
  padding-right: 80px;
  height: auto;
  /* overflow: initial; */
  top: 0;
  bottom: 0;
  /* position: fixed; */
  /* overflow-x: hidden; */
}
.current {
  display: block;
  flex-grow: 1;
  
}
.profile {
  padding-right: 150px;
  /* max-width: 516px; */
  height: 100vh;
}
.flex {
  display: flex;
}
span {
  color: rgb(148, 148, 149);
}

.socials-footer {
  display: none;
}
@media (max-width: 820px) {
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 60px;
    padding-right: 40px;
    overflow-x: hidden;
    display: block;
    position: relative;
    /* max-height: 100vh; */
  }
}

@media (max-width: 480px) {
  #app {
    margin-top: 40px;
    width: 100%;
  }
  .app {
    padding-left: 25px;
    padding-right: 25px;
    overflow-x: hidden;
    display: block;
    height: auto;
    overflow: initial;
  }
}
@media (max-width: 380px) {
  #app {
    margin-top: 20px;
    width: 100%;
  }
  .app {
    padding-left: 10px;
    padding-right: 10px;
  }
  .socials-footer {
    display: block;
    /* position: fixed; */
  }
}
@media (max-width: 360px) {
  #app {
    margin-top: 20px;
    width: 100%;
  }
  .app {
    padding-left: 30px;
    padding-right: 25px;
    overflow-x: hidden;
    display: block;
    height: auto;
    overflow: initial;
    width: 100%;
  }
  .socials-footer {
    display: block;
  }
}

@media (max-width: 280px) {
  #app {
    margin-top: 20px;
    width: 100%;
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 10px;
    padding-right: 10px;
    /* overflow-x: hidden; */
    display: block;
    overflow-y: auto;
    /* max-height: 100vh; */
    height: auto;
    overflow: initial;
    width: 100%;
  }
  .socials-footer {
    display: block;
  }
}
@media (max-width: 30px) {
  #app {
    margin-top: 20px;
    width: 100%;
  }
  .app {
    margin-left: auto;
    margin-right: auto;
    padding-left: 10px;
    padding-right: 10px;
    /* overflow-x: hidden; */
    display: block;
    overflow-y: auto;
    /* max-height: 100vh; */
    height: auto;
    overflow: initial;
  }
  .socials-footer {
    display: block;
  }
}
</style>
