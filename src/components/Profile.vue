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
        <li class="list-1 flex">
          <span>02</span>
          <div class="line"></div>
          PROJECT
        </li>
        <li class="list flex">
          <span>02</span>
          <div class="line"></div>
          TALK
        </li>
        <li class="list flex">
          <span>02</span>
          <div class="line"></div>
          INTERVIEWS
        </li>
      </ul>
    </div>
    <div class="profile-pics flex">
      <img src="../images/profile.png" alt="" />
      <div class="socials flex">
        <i class="lab la-github"></i>
        <p>github</p>
      </div>
      <div class="socials flex">
        <i class="lab la-facebook"></i>
        <p>Facebook</p>
      </div>
      <div class="socials flex">
        <i class="lab la-twitter"></i>
        <p>Twitter</p>
      </div>
      <div class="socials flex">
        <i class="lab la-linkedin-in"></i>
        <p>Linkedin-in</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
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
h1 {
  font-size: var(--fs-800);
  margin-bottom: 10px;
}
h2 {
  font-size: var(--fs-600);
  margin-bottom: 32px;
}
.about p {
  color: rgb(148, 148, 149);
  line-height: 1.9;
  width: 32em;
  font-size: 20px;
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
    font-size: var(--fs-600);
    width: 12em;
    margin-bottom: 10px;
  }
  h2 {
    font-size: var(--fs-400);
    margin-bottom: 32px;
  }
  .about p {
    line-height: 1.9;
    width: 28em;
    /* font-size: 16px; */
  }
  .skills {
    display: none;
  }
}
.about span {
  color: rgb(255, 255, 255);
  text-decoration: underline;
}
.line {
  background: hsl(var(--clr-light));
  width: 5em;
  height: 2px;
  margin: 10px 20px;
 
  cursor: pointer;
  cursor: pointer;
}
.line:hover {
  transition: all 0.2s ease-in-out;
  width: 6em;
  color: rgb(148, 148, 149);
}
.list-1 {
  
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
  color: hsl(var(--clr-light));
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
  /* background: hsl(var(--clr-light)); */
}

.skills {
  padding-top: 0px;
  letter-spacing: 3px;
}
.skills h3 {
  margin: 40px 0 0;
  color: rgb(148, 148, 149);
  font-size: 10px;
}
ul {
  list-style-type: none;
  padding: 30px 0px;
}
li {
  margin: 30px 10px;
}
.profile-pics {
  /* padding-top: 30px; */
  margin: -20px 0px;
  color: rgb(148, 148, 149);
}
.socials {
  padding: 0px 10px;
}
.lab {
  font-size: 28px;
  margin: 10px 10px;
}
img {
  width: 55px;
  height: 55px;
}
@media (max-width: 680px) {
  .lab {
    font-size: 18px;
    margin: 10px 10px;
  }
  .socials p {
    font-size: 12px;
  }
}
</style>
