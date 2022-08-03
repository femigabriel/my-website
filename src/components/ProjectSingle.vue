<template>
 
  <div :style="{ height: isRectangle ? 'auto' : '400px' }" class="project-box">
    <div class="status">
      <div class="framework">
        <p>{{ framework }}</p>
      </div>
      <div class="status">
        <p>{{ status }}</p>
      </div>

      <div class="date">
        <p>{{ date }}</p>
      </div>
    </div>
    <div class="title">
      <h2>{{ title }}</h2>
      <p>{{ description }}</p>
    </div>

    <div class="main flex">
      <div class="rating flex">
        <div class="icon"><i class="las la-external-link-alt"></i></div>
        <a target="_blank" :href="url">{{ video }}</a>
      </div>

      <div class="rating flex"></div>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    "framework",
    "isRectangle",
    "title",
    "status",
    "video",
    "date",
    "description",
    "url",
  ],
  data() {
    return {};
  },
};
</script>

<style scoped>
.project-box {
  width: 100%;
  background: rgb(32, 32, 34);
  padding: 40px;
  padding-bottom: 0;
  border-radius: 2px;
  cursor: pointer;
  line-height: 1.8;
  transition: all 0.2s ease-in-out;
}
.project-box:hover {
  width: 100%;
  box-shadow: 2px 9px 19px 15px #0000001f;
  transform: scale(1.1);
  -webkit-transition: all 200ms ease-in;
  -webkit-transform: scale(1.1);
  -ms-transition: all 200ms ease-in;
  -ms-transform: scale(1.1);
  -moz-transition: all 200ms ease-in;
  -moz-transform: scale(1.1);
  transition: all 200ms ease-in;
  padding-left: 40px;
  padding-right: 40px;
}
.status p {
  color: rgb(148, 148, 149);
  font-size: 14px;
}
.framework {
}

.framework p {
  letter-spacing: 5px;
  font-size: 12px;
  color: rgb(255, 255, 255);
}
.title .title h2 {
  line-height: 1.3;
  font-size: 22px;
}

.title p {
  color: rgb(148, 148, 149);
  font-size: 14px;
}

.main {
  padding-top: 30px;
}
.rating a {
  margin: 5px 10px;
  text-decoration: none;
  color: rgb(148, 148, 149);
  font-size: 14px;
  padding-bottom: 20px;
}
.icon {
}
.las {
  color: rgb(148, 148, 149);
  font-size: 20px;
  margin: 8px 2px;
}
.main p {
  font-size: 18px;
}
@media (max-width: 480px) {
  .projects {
    line-height: 1;
    width: 100%;
    overflow-x: hidden;
  }

  .project-box {
    /* width: 330px; */
    padding-top: 20px;
    padding-bottom: 40px;
  }
  .rating a {
    font-size: 12px;
  }
  .project-box h2 {
    font-size: 16px;
  }
  .project-box h3 {
    font-size: 12px;
  }
  .project-box p {
    line-height: 1.5;
    font-size: 12px;
    width: 10em;
  }
  .lar {
    font-size: 16px;
  }
}
@media (max-width: 420px) {
  .projects {
    line-height: 1;
    width: 100%;
    overflow-x: hidden;
  }
  .project-box {
    width: 100%;
    max-width: 315px;
    max-height: 33vh;
    line-height: 3.3;
  }
  

  .project-box h2 {
    font-size: 12px;
  }
  .project-box h3 {
    font-size: 12px;
  }
  .project-box p {
    line-height: 1.5;
    font-size: 12px;
    width: 14em;
  }
  .title {
  margin-top: 60px;
}
  .title h2 {
    line-height: 1.3;
    font-size: 18px;
    width: 10em;
    padding-top: 20px;
  }
  .lar {
    font-size: 12px;
  }
  .rating {
    /* margin: 15px 0px; */
  }
  .rating a {
    font-size: 9px;
  }
}
</style>
