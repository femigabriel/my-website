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
      
        <div v-show="current == 0" class="project-flex">
          <div class="project-flex-class">
            <div class="header">
              <h3>Projects</h3>
            </div>
            <ProjectFlex />
          </div>
          <ProjectGrid />
        </div>
        <div v-show="current == 1">
          <Resume />
        </div>
        <SocialFooter class="socials-footer" />
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
  height: auto;
  position: fixed;
}

.project-flex-class {
  margin-bottom: 10px;
}

.app {
  display: flex;
  margin-left: auto;
  margin-right: auto;
}
.current {
  display: block;
  flex-grow: 1;
  max-height: 100vh;
  overflow-y: auto;
  padding: 60px;
}

.flex {
  display: flex;
}
span {
  color: rgb(148, 148, 149);
}
.header {
  display: none;
}

.socials-footer {
  display: none;
}
.resume {
  display: block;
}
@media (max-width: 820px) {
  .app {
    margin-left: auto;
    margin-right: auto;
    overflow-x: hidden;
    display: block;
    position: relative;
  }
}

@media (max-width: 420px) {
  body {
    position: relative;
  }

  .socials-footer {
    display: block;
  }
  .current {
    max-height: initial;
    padding: 20px;
  }
  .header {
    color: rgb(255, 255, 255);
    padding: 10px 0px;
    display: block;
    font-weight: 700;
    font-size: 12px;
    padding-top: 30px;
    padding-bottom: 20px;
    position: sticky;
    letter-spacing: 5px;
    text-transform: uppercase;
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
  .header {
    color: rgb(255, 255, 255);
    padding: 10px 0px;
    display: block;
    font-weight: 700;
    font-size: 12px;
    padding-top: 30px;
    position: sticky;
    letter-spacing: 3px;
    text-transform: uppercase;
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
