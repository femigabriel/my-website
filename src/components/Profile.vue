<template>
  <div class="profile">
    <div class="profile-name">
      <h1>Gabriel Femi</h1>
      <h2>Staff Software Engineer at Google</h2>
    </div>
    <div class="about">
      <p>
        I build open-source front-end libraries at <span>Algolia</span> and host
        two tech podcasts: <span>Developer Experience</span> and
        <span>Entre Devs</span>. On my spare time, I share what I learn on my
        <span>blog</span> and speak at <span>tech conferences</span> around the
        world.
      </p>
    </div>
    <div class="skills">
      <ul class="">
        <li
          v-bind:class="{ active: li.id === activeId }"
          v-on:click="setActivePage(li.id)"
          class="list flex"
          v-for="li in lists"
          :key="li"
        >
          <span>{{ li.numb }}</span>
          <div class="flex" v-bind:class="{ active: li.id === activeId }">
            <div class="line"></div>
            {{ li.status }}
          </div>
        </li>
      </ul>
    </div>
    <div class="profile-pics flex">
      <img src="../images/mypics4.png" alt="" />
      <div class="socials flex">
        <i class="lab la-github"></i>
        <a href="https://github.com/femigabriel">github</a>
        <p></p>
      </div>
      <div class="socials flex">
        <i class="lab la-facebook"></i>
        <a href="facebook.com/femigabriel89">Facebook</a>
        <p></p>
      </div>
      <div class="socials flex">
        <i class="lab la-twitter"></i>
        <a href="https://twitter.com/FemiGab2018">Twitter</a>
        <p></p>
      </div>
      <div class="socials flex">
        <i class="lab la-linkedin"></i>
        <a href="https://www.linkedin.com/in/ogungbade-oluwafemi-25b28619a/"
          >Linkedin</a
        >
        <p></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["activeId"],
  data() {
    return {
      lists: [
        { id: 0, numb: "01", status: "PROJECT" },
        { id: 1, numb: "02", status: "RESUME" },
        // { id: 2, numb: "03", status: "WORK" },
      ],
    };
  },
  emits: [],
  methods: {
    setActivePage(value) {
      this.$emit("setActivePage", value);
    },
    // selectedList(id) {
    //   this.activeId = id;
    // },
  },
};
</script>
<style scoped>
.profile {
  display: flex;
  flex-direction: column;
}
.profile-name {
  line-height: 1;
}
.profile-name h1 {
  /* font-size: 6.8em; */
  font-size: 68px;
  margin-bottom: 10px;
}
h2 {
  font-size: 24px;
  margin-bottom: 32px;
}

.about p {
  color: rgb(148, 148, 149);
  line-height: 1.9;
  width: 30em;
  font-size: 14px;
}
@media (max-width: 680px) {
  .profile {
    display: flex;
    flex-direction: column;
  }
  .profile-name {
    line-height: 1;
  }
  h1 {
    font-size: 3em;
    width: 12em;
    margin-bottom: 10px;
  }
  h2 {
    font-size: 1em;
    margin-bottom: 32px;
    width: 18em;
  }

  .skills {
    display: none;
  }
  .about p {
    line-height: 1.5;
    width: 17em;
    font-size: 13px;
    padding-bottom: 20px;
  }
  .profile-pics {
  }
}
.about span {
  color: rgb(255, 255, 255);
  text-decoration: underline;
}
.line {
  background: rgb(255, 255, 255);
  width: 5em;
  height: 2px;
  margin: 10px 20px;
  cursor: pointer;
}
.line:hover {
  transition: all 0.2s ease-in-out;
  width: 6em;
  color: rgb(148, 148, 149);
}
.active {
  color: rgb(255, 255, 255);
}
.list-1:hover {
  color: rgb(148, 148, 149);
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}
.list {
  color: rgb(148, 148, 149);
  cursor: pointer;
}
.list:hover {
  color: rgb(255, 255, 255);
  transition: all 0.2s ease-in-out;
}

.list .line {
  cursor: pointer;
  background: rgb(148, 148, 149);
  width: 3em;
  cursor: pointer;
}
.list .line:hover {
  width: 5em;
  transition: all 0.2s ease-in-out;
}
.list .line:active {
  width: 6em;
  transition: all 0.2s ease-in-out;
  color: rgb(255, 255, 255);
}
.skills {
  padding-top: 0px;
  letter-spacing: 3px;
  margin: -30px 0px;
}
ul {
  list-style-type: none;
  padding: 30px 0px;
}
li {
  margin: 30px 10px;
}
.profile-pics {
  margin: -20px 0px;
  color: rgb(148, 148, 149);
}
.socials {
  padding: 5px 5px;
}
.socials a {
  color: rgb(255, 255, 255);
  font-size: 1em;
  margin: 15px 0px;
  text-decoration: none;
}
.lab {
  font-size: 24px;
  margin: 10px 5px;
}
img {
  width: 55px;
  height: 55px;
  border-radius: 50%;
}
@media (max-width: 680px) {
  .lab {
    font-size: 10px;
    margin: 6px 5px;
  }
  .socials {
    padding: 5px 8px;
  }
  .socials p {
    font-size: 8px;
  }

  .profile-pics {
    padding-bottom: 20px;
  }
}
</style>
