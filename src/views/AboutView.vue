<template>
  <div class="about-container">
    <div class="about-wrapper">
      <div class="about-img">
        <img
          :src="profilePic"
          class="abt-pic"
          :class="[profilePic == !'' ? 'abt-pic' : 'abt-skeleton']"
        />
      </div>
      <div class="about-content">
        <div class="abt-info">
          <h2>about me</h2>
          <h3>software developer & graphic designer</h3>
          <p>
            My name is <strong> collins odongo, </strong> a passionate
            <strong> designer </strong> and
            <strong> fullstack developer </strong> based in Nairobi, Kenya and
            highly addicted to coffee. am a problem solver and a pioneer of good
            designs so your projects are safe with me
          </p>
        </div>
        <div class="abt-skill-progress">
          <div
            class="progress-bar"
            v-for="({ Sname, Skill, Scolor }, index) in skills"
            :key="index"
          >
            <label>{{ Sname }}</label>
            <div class="skill-bar">
              <span :style="{ width: Skill + '%' }">
                <span class="progress" :style="{ backgroundColor: Scolor }">
                </span
              ></span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="work-container">
      <WorkInfo />
    </div>
    <div class="techStack-c">
      <h1>Tech stacks 👨‍💻</h1>
      <TechStack />
    </div>
  </div>
</template>
<script setup>
import WorkInfo from "../components/WorkInfo.vue";
import TechStack from "../components/TechStack.vue";
</script>
<script>
export default {
  data() {
    return {
      components: {
        WorkInfo,
        TechStack,
      },
      skills: [
        {
          Sname: "web development",
          Scolor: "#5db85d",
          Skill: 98,
        },

        {
          Sname: "app development",
          Scolor: "#d8524f",
          Skill: 90,
        },
        {
          Sname: "graphic design",
          Scolor: "#337ab6",
          Skill: 87,
        },
        {
          Sname: "UX UI design",
          Scolor: "#5ac0df",
          Skill: 78,
        },
        {
          Sname: "Dev ops",
          Scolor: "#f1ac4e",
          Skill: 70,
        },
      ],

      languages: [
        {
          Lname: "javascript",
          level: 98,
        },
        {
          Lname: "Golang",
          level: 86,
        },
        {
          Lname: "python",
          level: 90,
        },
        {
          Lname: "Dart",
          level: 70,
        },
        {
          Lname: "c+",
          level: 75,
        },
      ],
      profilePic: "https://avatars.githubusercontent.com/u/86556838",
    };
  },
};
</script>

<style>
@import "../style/AboutView.css";
</style>
