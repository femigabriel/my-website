<template>
  <div class="resume"></div>
  <div class="pages_container">
    <div class="resume">
      <div class="resume_container">
        <div class="top_row">
          <h2>GABRIEL FEMI(TIMFEMI@GMAIL.COM)</h2>
        </div>
        <p class="subheading">Frontend Developer</p>
        <div class="summary">
          <p>
            Passionate front-end developer with a desire to learn and
            grow in a collaborative team environment. Skilled in HTML, CSS, and
            JavaScript. Excels at creating pixel-perfect designs and working
            with cross-browser compatibility issues.
          </p>
        </div>
        <div class="divider">
          <p>Core Technologies</p>
          <span></span>
        </div>
        <div class="skills">
          <p>HTML/CSS/SASS, Javascript, Vue JS, React JS</p>
        </div>
        <!-- <div class="divider">
          <p>Familiar With</p>
          <span></span>
        </div> -->
        <!-- <div class="skills">
          <p>
            Node JS, Express, Nuxt JS, Unit Testing, Web Sockets, PWAs,
            Wordpress, SEO.
          </p>
        </div> -->
        <!-- <div class="divider">
          <p>On The Job</p>
          <span></span>
        </div> -->
        <!-- <div class="skills">
          <p>Agile/Scrum, Version Control, Best Practices, CI/CD</p>
        </div> -->
        <div class="divider">
          <p>Work Experience</p>
          <span></span>
        </div>
        <div class="exp_container">
        
        </div>
        <div class="divider">
          <p>Projects</p>
          <span></span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
p {
  font-size: 12px;
}
.pages_container {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  justify-content: space-between;
  /* padding: 2% 15% 10% 5%; */
}

.resume_container {
  background-color: #1b1b1d;
  display: flex;
  flex-direction: column;
  padding: 5%;
}
.top_row {
  align-items: center;
  display: flex;
  justify-content: space-between;
}
.top_row h2 {
  font-size: 14px;
  line-height: 47px;
  margin: 0;
  letter-spacing: 5px;
}

small {
  font-size: smaller;
}
.fa,
.fab,
.fad,
.fal,
.far,
.fas {
  display: inline-block;
  line-height: 1;
}
.subheading {
  color: #cfcfcf;
  font-size: 14px;
  margin: 6px 0;
  letter-spacing: 3px;
}
.summary {
  display: flex;
  margin-top: 5px;
}
.summary p {
  color: rgb(148, 148, 149);
  font-size: 14px;
  line-height: 1.9;
}
.divider {
  align-items: center;
  display: flex;
  margin-bottom: 15px;
  margin-top: 15px;
}
.divider p {
  color: #e2e2e2;
  font-size: 14px;
  font-weight: 600;
  margin: 0 10px 0 0;
  /* letter-spacing: 5px; */
}
.divider span {
  background-color: #77777859;
  flex-grow: 1;
  height: 1px;
}
.skills p {
  color: #777778;
  display: flex;
  font-size: 14px;
  line-height: 1.9;
  margin: 0;
}
.divider {
  align-items: center;
  display: flex;
  margin-bottom: 15px;
  margin-top: 15px;
}
.divider span {
  background-color: #77777859;
  flex-grow: 1;
  height: 1px;
}
section {
  display: block;
}
.experience .title {
  font-size: 14px;
  line-height: 2;
  margin: 0;
  letter-spacing: 3px;
  text-transform: uppercase;
}
.experience .description {
  color: #777778;
  display: block;
  font-size: 14px;
  line-height: 1.9;
  margin: 10px 0;
  padding: 0;
}
.description p {
  color: #777778;
  display: flex;
  margin: 2px 0;
  width: 100%;
  font-size: 14px;
}

.description p span {
  margin-right: 5px;
  color: #777778;
  font-size: 14px;
}
.resume_container .divider {
  align-items: center;
  display: flex;
  margin-bottom: 15px;
  margin-top: 15px;
}
.divider span {
  background-color: #77777859;
  flex-grow: 1;
  height: 1px;
}
.description p.nospan {
  display: block;
  font-size: 14px;
}
@media (max-width: 820px) {
  .pages_container {
    padding: 10px 10px;
    width: 700px;
    margin-left: -10px;
  }
}
@media (max-width: 720px) {
  .pages_container {
    padding: 10px 10px;
    width: 100%;
  }
}
@media (max-width: 480px) {
  .pages_container {
    padding: 10px 10px;
    width: 100%;
  }
}

@media (max-width: 360px) {
  .pages_container {
    padding: 10px 5px;
    width: 100%;
  }
  /* .top_row h2 {
    font-size: 14px;
  }
  summary p {
    font-size: 9px;
    line-height: 1.9;
  }
  .description p span {
  margin-right: 5px;
  color: #777778;
  font-size: 9px;
} */
}
</style>
