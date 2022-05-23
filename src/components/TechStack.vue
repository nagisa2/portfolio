<template>
  <div class="tech-stack-layout">
    <div
      class="language stack"
      v-for="({ languageIcon, languageName }, index) in Languages"
      :key="index"
    >
      <img class="work-icon" :src="languageIcon" :alt="{ languageName }" />
      <h4>{{ languageName }}</h4>
    </div>
    <div
      class="design stack"
      v-for="({ designIcon, designName }, index) in DesignStack"
      :key="index"
    >
      <img class="work-icon" :src="designIcon" :alt="{ designName }" />
      <h4>{{ designName }}</h4>
    </div>
    <div
      class="framework stack"
      v-for="({ frameIcon, frameName }, index) in FrameWork"
      :key="index"
    >
      <img class="work-icon" :src="frameIcon" :alt="{ frameName }" />
      <h4>{{ frameName }}</h4>
    </div>
    <div
      class="database stack"
      v-for="({ databaseIcon, databaseName }, index) in DatabaseStack"
      :key="index"
    >
      <img class="work-icon" :src="databaseIcon" :alt="{ databaseName }" />
      <h4>{{ databaseName }}</h4>
    </div>
    <div class="animation stack">
      <svg class="work-icon" viewBox="0 0 14 21">
        <path d="M0 0h14v7H7zm0 7h7l7 7H7v7l-7-7z" fill="currentColor"></path>
      </svg>
      <h4>framer motion</h4>
    </div>
    <div class="animation stack">
      <img
        class="work-icon "
        src="https://cdn.worldvectorlogo.com/logos/gsap-greensock.svg"
        alt="GreenSock"
      />
      <h4>GreenSock</h4>
    </div>
    <div
      class="devops stack" 
      v-for="({ devopIcon, devopName }, index) in DevopStack"
      :key="index"
    >
      <img class="work-icon" :src="devopIcon" :alt="{ devopName }" />
      <h4>{{ devopName }}</h4>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Languages: [
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/coffeescript/coffeescript-original.svg",
          languageName: "Coffeescript",
        },
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dart/dart-original.svg",
          languageName: "Dart",
        },
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-plain.svg",
          languageName: "JavaScript",
        },
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg",
          languageName: "Golang",
        },
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg",
          languageName: "Python",
        },
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/ruby/ruby-original.svg",
          languageName: "ruby",
        },
        {
          languageIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg",
          languageName: "C",
        },
      ],
      DesignStack: [
        {
          designIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/illustrator/illustrator-plain.svg",
          designName: "Illustrator",
        },
        {
          designIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/photoshop/photoshop-plain.svg",
          designName: "Photoshop",
        },
        {
          designIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/inkscape/inkscape-original.svg",
          designName: "Inkscape",
        },
        {
          designIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg",
          designName: "Figma",
        },
        {
          designIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gimp/gimp-original.svg",
          designName: "Gimp",
        },
      ],
      FrameWork: [
        {
          frameIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg",
          frameName: "Reactjs",
        },
        {
          frameIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg",
          frameName: "Vuejs",
        },
        {
          frameIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original.svg",
          frameName: "Nexjs",
        },
        {
          frameIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flutter/flutter-original.svg",
          frameName: "Flutter",
        },
        {
          frameIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
          frameName: "Nodejs",
        },
        {
          frameIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/firebase/firebase-plain.svg",
          frameName: "Firebase",
        },
      ],
      DatabaseStack: [
        {
          databaseIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mongodb/mongodb-original.svg",
          databaseName: "Mongodb",
        },
        {
          databaseIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
          databaseName: "MySql",
        },
        {
          databaseIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg",
          databaseName: "Sqlite",
        },
      ],
      DevopStack: [
        {
          devopIcon:
            "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg",
          devopName: "Docker",
        },
      ],
    };
  },
};
</script>

<style>
@import "../style/TechStack.css";
</style>
