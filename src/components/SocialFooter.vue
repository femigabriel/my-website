<template>
  <footer>
    <div class="profile-pics flex">
      <img src="../images/mypics4.png" alt="" />
      <div class="socials flex">
        <a href="https://github.com/femigabriel">
          <i class="lab la-github"></i>Github</a
        >
      </div>
      <div class="socials flex">
        <a href="facebook.com/femigabriel89">
          <i class="lab la-facebook"></i>Facebook</a
        >
      </div>
      <div class="socials flex">
        <a href="https://twitter.com/FemiGab2018">
          <i class="lab la-twitter"></i>Twitter</a
        >
      </div>
      <div class="socials flex">
        <a href="https://www.linkedin.com/in/ogungbade-oluwafemi-25b28619a/">
          <i class="lab la-linkedin"></i>Linkedin</a
        >
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
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
  margin: 20px 0px;
  color: rgb(148, 148, 149);
}
.socials {
  padding: 15px 5px;
}
.socials a {
  color: rgb(255, 255, 255);
  font-size: 14px;
  margin: 2px 7px;
  text-decoration: none;
}
.lab {
  font-size: 24px;
  margin: 3px 10px;
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
    margin: 15px 0px;
  }
}
@media (max-width: 380px) {
  .lab {
    font-size: 24px;
    margin-bottom: 5px;
  }
  .socials {
    padding: 2px 0px;
  }
  .socials a {
    font-size: 7px;
    margin: 5px 5px;
    /* display: none; */
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
</style>
