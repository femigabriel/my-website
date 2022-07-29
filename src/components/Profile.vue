<template>
  <div class="profile">
    <div class="profile-name">
      <h1>Gabriel Femi</h1>
      <h2>Staff Software Engineer</h2>
    </div>
    <div class="about">
      <p>
        i'm a passionate junior front-end developer with a desire to learn and
        grow in a collaborative team environment. I'm Skilled in HTML, CSS, and
        JavaScript.
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
          <div></div>
          <span v-bind:class="{ active: li.id === activeId }">{{
            li.numb
          }}</span>
          <div class="flex" v-bind:class="{ active: li.id === activeId }">
            <div v-bind:class="{ lineActive: li.id === activeId }">
              <div class="line"></div>
            </div>

            {{ li.status }}
          </div>
        </li>
      </ul>
    </div>
    <div class="profile-pics flex">
      <img src="../images/mypics4.png" alt="" />
      <div class="socials flex">
        <i class="lab la-github"></i>
        <a href="https://github.com/femigabriel">Github</a>
      </div>
      <div class="socials flex">
        <i class="lab la-facebook"></i>
        <a href="facebook.com/femigabriel89">Facebook</a>
      </div>
      <div class="socials flex">
        <i class="lab la-twitter"></i>
        <a href="https://twitter.com/FemiGab2018">Twitter</a>
      </div>
      <div class="socials flex">
        <i class="lab la-linkedin"></i>
        <a href="https://www.linkedin.com/in/ogungbade-oluwafemi-25b28619a/"
          >Linkedin</a
        >
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
@media (max-width: 680px) {
  .profile-name h1 {
    font-size: 38px;
  }
}
.profile-name h1 {
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
@media (max-width: 480px) {
  .profile-name h1 {
    font-size: 45px;
    margin-bottom: 10px;
  }
  .profile-name h2 {
    font-size: 1.4em;
    margin-bottom: 32px;
    width: 18em;
  }

  .skills {
    display: block;
  }
  .about p {
    line-height: 1.5;
    width: 28em;
    font-size: 12px;
    padding-bottom: 20px;
  }
  .profile-pics {
  }
}
@media (max-width: 320px) {
  .profile {
    display: flex;
    flex-direction: column;
  }
  .profile-name {
    line-height: 1;
  }
  .profile-name h1 {
    font-size: 32px;
    width: 12em;
    margin-bottom: 10px;
  }
  .profile-name h2 {
    font-size: 1em;
    margin-bottom: 32px;
    width: 18em;
  }
  .skills {
    display: block;
  }
  .about p {
    line-height: 1.5;
    width: 20em;
    font-size: 12px;
    padding-bottom: 20px;
  }
  .profile-pics {
  }
}
@media (max-width: 280px) {
  .profile {
    display: flex;
    flex-direction: column;
  }
  .profile-name {
    line-height: 1;
  }
  .profile-name h1 {
    font-size: 32px;
    color: red;
    width: 12em;
    margin-bottom: 10px;
  }
  .profile-name h2 {
    font-size: 1em;
    margin-bottom: 32px;
    width: 18em;
  }

  .skills {
    display: block;
    /* font-size: 14px; */
  }
  .about p {
    line-height: 1.5;
    width: 20em;
    font-size: 12px;
    padding-bottom: 20px;
  }
  .profile-pics {
  }
}
/* @media (max-width: 320px) {
} */
.about span {
  color: rgb(255, 255, 255);
  text-decoration: underline;
}
.line {
  background: rgb(255, 255, 255);
  width: 5em;
  height: 2px;
  margin: 5px 20px;
  cursor: pointer;
}

.active {
  color: rgb(255, 255, 255);
}
.lineActive {
  background: rgb(255, 255, 255);
  height: 2px;
  margin: 5px 10px;
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
  margin: 0px 15px;
}
.list .line:hover {
  width: 5em;
  transition: all 0.2s ease-in-out;
  background: rgb(255, 255, 255);
}
.skills {
  padding-top: 10px;
  margin: -10px 0px;
}
ul {
  list-style-type: none;
  padding: 30px 0px;
}
li {
  font-size: 10px;
  margin: 45px 10px;
  letter-spacing: 5px;
}
.profile-pics {
  margin: 10px 0px;
  color: rgb(148, 148, 149);
}
.socials {
  padding: 5px 5px;
}
.socials a {
  color: rgb(255, 255, 255);
  font-size: 14px;
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

@media (max-width: 480px) {
  .lab {
    font-size: 16px;
    margin-bottom: 5px;
  }
  .socials {
    padding: 5px 2px;
  }
  .socials a {
    font-size: 12px;
    margin-top: 12px;
  }

  .profile-pics {
    padding-bottom: 20px;
  }
  img {
    width: 45px;
    height: 45px;
    border-radius: 50%;
  }
}
@media (max-width: 320px) {
  .lab {
    font-size: 12px;
    margin-bottom: 5px;
  }
  .socials {
    padding: 2px 0px;
  }
  .socials a {
    font-size: 7px;
    margin-top: 12px;
  }

  .profile-pics {
    padding-bottom: 20px;
  }
  img {
    width: 35px;
    height: 35px;
    border-radius: 50%;
  }
}
</style>
