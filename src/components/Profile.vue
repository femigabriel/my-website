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
.profile-name h1 {
  font-size: 6.8em;
  margin-bottom: 10px;
}
h2 {
  font-size: 2.2em;
  margin-bottom: 32px;
}
.about p {
  color: rgb(148, 148, 149);
  line-height: 1.9;
  width: 26em;
  font-size: 1.7em;
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
  font-size: 14px;
  padding-bottom: 20px;
}
.profile-pics{

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

.skills {
  padding-top: 0px;
  letter-spacing: 3px;
}
/* .skills h3 {
  margin: 40px 0 0;
  color: rgb(148, 148, 149);
  font-size: 2em;
} */
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
  padding: 5px 10px;
}
 .socials p {
    font-size: 1.2em;   
    /* margin: 15px 0px; */
  }
.lab {
  font-size: 28px;
  margin: 8px 10px;
}
img {
  width: 55px;
  height: 55px;
}
@media (max-width: 680px) {
  .lab {
    font-size: 13px;
    margin: 6px 5px;
  }
  .socials {
  padding: 5px 8px;
}
  .socials p {
    font-size: 9px;
   
  }
  img {
  width: 35px;
  height: 35px;
}
.profile-pics {
  padding-bottom: 20px;
}
}
</style>
