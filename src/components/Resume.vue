<template>
  <div class="resume"></div>
  <div class="pages_container">
    <div class="resume">
      <div class="resume_container">
        <div class="top_row">
          <h2>GABRIEL FEMI</h2>
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
          <p>HTML/CSS/SASS, Javascript [ES6+], Vue.JS, .</p>
        </div>
        <div class="divider">
          <p>Familiar With</p>
          <span></span>
        </div>
        <div class="skills">
          <p>
            Node JS, Express, Nuxt JS, Unit Testing, Web Sockets, PWAs,
            Wordpress, SEO.
          </p>
        </div>
        <div class="divider">
          <p>On The Job</p>
          <span></span>
        </div>
        <div class="skills">
          <p>Agile/Scrum, Version Control, Best Practices, CI/CD</p>
        </div>
        <div class="divider">
          <p>Work Experience</p>
          <span></span>
        </div>
        <div class="exp_container">
          <section class="experience">
            <p class="title">
              Caketools<!-- -->
              - <i>Frontend Engineer</i
              ><span
                ><br />
                <!-- -->MAY 2021<!-- -->
                -<!-- -->
                <!-- -->PRESENT</span
              >
            </p>
            <article class="description">
              <p>
                <!-- -->I’m currently building smart solutions on the
                decentralised web with the team at Caketools labs<!-- -->
              </p>
              <p>
                <span>■</span>
                <!-- -->Crafted a component library from scratch using SCSS
                Modules to ensure consistency.
              </p>
              <p>
                <span>■</span>
                <!-- -->Used Next Js to deliver optimised, pre-rendered pages
                when necessary.
              </p>
              <p>
                <span>■</span>
                <!-- -->Engineered state management with Redux and Hooks.
              </p>
              <p>
                <span>■</span>
                <!-- -->Pulled data from the blockchain in real time to display
                live statistics and token prices.
              </p>
              <p>
                <span>■</span>
                <!-- -->Visualized blockchain data using charting libraries and
                custom paginated tables.
              </p>
              <p>
                <span>■</span>
                <!-- -->Maintained a well structured codebase and used
                Typescript to improve predictability.
              </p>
              <p>
                <span>■</span>
                <!-- -->Integrated seamless blockchain wallet connection with
                support for about six different wallet providers.
              </p>
              <p>
                <span>■</span>
                <!-- -->Implemented api request caching on the server to save
                resources, improve performance and generally reduce load on the
                backend.
              </p>
            </article>
          </section>
          <section class="experience">
            <p class="title">
              Playarone<!-- -->
              - <i>Frontend Developer [Contract]</i
              ><span
                ><br />
                <!-- -->SEPTEMBER 2020<!-- -->
                -<!-- -->
                <!-- -->OCTOBER 2021</span
              >
            </p>
            <article class="description">
              <p>
                <!-- -->I Joined the Playarone engineering team in building an
                e-sports gaming platform.<!-- -->
              </p>
              <p>
                <span>■</span>
                <!-- -->Built complex layouts and components with React &amp;
                SASS
              </p>
              <p>
                <span>■</span>
                <!-- -->Managed app state with react hooks
              </p>
              <p>
                <span>■</span>
                <!-- -->Worked closely with a senior engineer to implement app
                features with a postgres database, typescript and the MVC
                pattern.
              </p>
            </article>
          </section>
          <section class="experience">
            <p class="title">
              Charisol<!-- -->
              - <i>Frontend Developer [Contract]</i
              ><span
                ><br />
                <!-- -->OCTOBER 2020<!-- -->
                -<!-- -->
                <!-- -->MARCH 2021</span
              >
            </p>
            <article class="description">
              <p>
                <!-- -->I worked with the charisol product team on a contract
                basis to build a web application for a fintech startup<!-- -->
              </p>
              <p>
                <span>■</span>
                <!-- -->Transformed figma prototypes for a fintech application
                to a functional UI using react js combined with context api for
                state management and sass for styling.
              </p>
              <p>
                <span>■</span>
                <!-- -->Made use of tools like Notion &amp; Usepastel for task
                management and feedback
              </p>
              <p>
                <span>■</span>
                <!-- -->Interacted with GraphQL apis from the client side using
                Apollo GraphQL
              </p>
            </article>
          </section>
          <section class="experience">
            <p class="title">
              HNG Internships<!-- -->
              - <i>Frontend Developer [Intern]</i
              ><span
                ><br />
                <!-- -->MAY 2020<!-- -->
                -<!-- -->
                <!-- -->AUGUST 2020</span
              >
            </p>
            <article class="description">
              <p>
                <!-- -->I contributed in developing user interfaces for quite a
                number of products within three months while learning new skills<!-- -->
              </p>
              <p>
                <span>■</span>
                <!-- -->Worked with node.js developers to build a certificate
                generator
              </p>
              <p>
                <span>■</span>
                <!-- -->Headed the frontend department of my team to deliver
                responsive web templates to be sold on envato market
              </p>
              <p>
                <span>■</span>
                <!-- -->Built an open source micro API project alongside python
                (Django) Developers using Jinja template engine on the frontend
              </p>
            </article>
          </section>
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
