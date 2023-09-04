<template>
  <div class="portfolio-container">
    <div class="portfolio-content">
      <div class="portfolio-header">
        <h1>Some of the projects I've done</h1>
        <h3>For more, visit my social media platforms</h3>
      </div>
      <div
        class="portfolio-wrapper"
        v-for="{
          projectType,
          projectTitle,
          projectImage,
          projectDescription,
          toolsUsed
        } in Projects"
        :key="projectTitle"
      >
        <div class="portfolio-img" :class="[ projectImage == !'' ? 'portfolio-img' : 'portfolio-skeleton', ]">
          <img class="img-wrapper" :src="projectImage" :alt="projectTitle" />
        </div>
        <div class="portfolio-info">
          <h3>{{ projectType }}</h3>
          <h1>{{ projectTitle }}</h1>
          <div class="info-details">
            <p>{{ projectDescription }}</p>
          </div>
          <div class="tool-wrapper">
            <div class="tools-used">
              <span>{{ toolsUsed.adobe }}</span>
              <span>{{ toolsUsed.photoshop }}</span>
            </div>
            <div class="tools-used">
              <span>{{ toolsUsed.framework }}</span>
               <span>{{ toolsUsed.server }}</span>
               <span>{{ toolsUsed.translation }}</span>
            </div>
          </div>
          <div class="portfolio-link">
            <div v-if="projectType === 'Web development'">
              <svg
                class="icon h-icon"
                viewBox="0 0 24 24"
                @click="githubProject(projectTitle)"
              >
              <path
                  fill="currentColor"
                  d="M12,2A10,10 0 0,0 2,12C2,16.42 4.87,20.17 8.84,21.5C9.34,21.58 9.5,21.27 9.5,21C9.5,20.77 9.5,20.14 9.5,19.31C6.73,19.91 6.14,17.97 6.14,17.97C5.68,16.81 5.03,16.5 5.03,16.5C4.12,15.88 5.1,15.9 5.1,15.9C6.1,15.97 6.63,16.93 6.63,16.93C7.5,18.45 8.97,18 9.54,17.76C9.63,17.11 9.89,16.67 10.17,16.42C7.95,16.17 5.62,15.31 5.62,11.5C5.62,10.39 6,9.5 6.65,8.79C6.55,8.54 6.2,7.5 6.75,6.15C6.75,6.15 7.59,5.88 9.5,7.17C10.29,6.95 11.15,6.84 12,6.84C12.85,6.84 13.71,6.95 14.5,7.17C16.41,5.88 17.25,6.15 17.25,6.15C17.8,7.5 17.45,8.54 17.35,8.79C18,9.5 18.38,10.39 18.38,11.5C18.38,15.32 16.04,16.16 13.81,16.41C14.17,16.72 14.5,17.33 14.5,18.26C14.5,19.6 14.5,20.68 14.5,21C14.5,21.27 14.66,21.59 15.17,21.5C19.14,20.16 22,16.42 22,12A10,10 0 0,0 12,2Z"
                />
              </svg>
            </div>
            <div v-else>
              <svg
                class="icon h-icon"
                @click="behanceProject(projectTitle)"
                viewBox="0 0 16 16"
              >
              <path
                  fill="currentColor"
                  d="M4.654 3c.461 0 .887.035 1.278.14.39.07.711.216.996.391.286.176.497.426.641.747.14.32.216.711.216 1.137 0 .496-.106.922-.356 1.242-.215.32-.566.606-.997.817.606.176 1.067.496 1.348.922.281.426.461.957.461 1.563 0 .496-.105.922-.285 1.278a2.317 2.317 0 0 1-.782.887c-.32.215-.711.39-1.137.496a5.329 5.329 0 0 1-1.278.176L0 12.803V3h4.654zm-.285 3.978c.39 0 .71-.105.957-.285.246-.18.355-.497.355-.887 0-.216-.035-.426-.105-.567a.981.981 0 0 0-.32-.355 1.84 1.84 0 0 0-.461-.176c-.176-.035-.356-.035-.567-.035H2.17v2.31c0-.005 2.2-.005 2.2-.005zm.105 4.193c.215 0 .426-.035.606-.07.176-.035.356-.106.496-.216s.25-.215.356-.39c.07-.176.14-.391.14-.641 0-.496-.14-.852-.426-1.102-.285-.215-.676-.32-1.137-.32H2.17v2.734h2.305v.005zm6.858-.035c.286.285.711.426 1.278.426.39 0 .746-.106 1.032-.286.285-.215.46-.426.53-.64h1.74c-.286.851-.712 1.457-1.278 1.848-.566.355-1.243.566-2.06.566a4.135 4.135 0 0 1-1.527-.285 2.827 2.827 0 0 1-1.137-.782 2.851 2.851 0 0 1-.712-1.172c-.175-.461-.25-.957-.25-1.528 0-.531.07-1.032.25-1.493.18-.46.426-.852.747-1.207.32-.32.711-.606 1.137-.782a4.018 4.018 0 0 1 1.493-.285c.606 0 1.137.105 1.598.355.46.25.817.532 1.102.958.285.39.496.851.641 1.348.07.496.105.996.07 1.563h-5.15c0 .58.21 1.11.496 1.396zm2.24-3.732c-.25-.25-.642-.391-1.103-.391-.32 0-.566.07-.781.176-.215.105-.356.25-.496.39a.957.957 0 0 0-.25.497c-.036.175-.07.32-.07.46h3.196c-.07-.526-.25-.882-.497-1.132zm-3.127-3.728h3.978v.957h-3.978v-.957z"
                />
              </svg>
            </div>
            <svg
              class="icon h-icon"
              viewBox="0 0 24 24"
              v-if="projectType === 'Graphic design'"
              @click="graphicLink(projectTitle)"
            >
            <path
                fill="currentColor"
                d="M14,3V5H17.59L7.76,14.83L9.17,16.24L19,6.41V10H21V3M19,19H5V5H12V3H5C3.89,3 3,3.9 3,5V19A2,2 0 0,0 5,21H19A2,2 0 0,0 21,19V12H19V19Z"
              />
            </svg>
            <svg
              class="icon h-icon"
              viewBox="0 0 24 24"
              @click="webLink(projectTitle)"
              v-else
            >
            <path
                fill="currentColor"
                d="M14,3V5H17.59L7.76,14.83L9.17,16.24L19,6.41V10H21V3M19,19H5V5H12V3H5C3.89,3 3,3.9 3,5V19A2,2 0 0,0 5,21H19A2,2 0 0,0 21,19V12H19V19Z"
              />
            </svg>
          </div>
        </div>
      </div>
      <div class="cv-button">
        <a
          class="portfolio-btn"
          href="/cv.pdf"
          download
          id="btn"
        >
          Download CV
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<script>
export default {
  data() {
    return {
      Projects: [
        {
          projectType: "Web development",
          githubLink: "https://github.com/zero-stealth/prediction",
          projectLink: "https://sportypredict.com/",
          projectImage:
            "https://raw.githubusercontent.com/zero-stealth/portfolio/master/src/assets/po1.jpg",
          projectTitle: "Sporty predict",
          projectDescription:
            "Sporty predict is tips and statistics provider about football-related contents",
          toolsUsed: {
            framework: "Vue.js",
            server: "Nodejs",
            translation: "i8n",
          },
        },
        {
          projectType: "Web development",
          githubLink: "https://github.com/zero-stealth/dusstech",
          projectLink: "https://dusstech-brands.vercel.app/",
          projectImage:
            "https://raw.githubusercontent.com/zero-stealth/portfolio/master/src/assets/po2.jpg",
          projectTitle: "Dusstech brands",
          projectDescription:
            "Dusstech brands is a design and branding agency in Nairobi",
          toolsUsed: {
            framework: "Vue.js",
            server: "Nodejs",
          },
        },
        {
          projectType: "Graphic design",
          behanceLink:
            "https://www.behance.net/",
          projectImage:
            "https://raw.githubusercontent.com/zero-stealth/portfolio/master/src/assets/banner.png",
          projectTitle: "poster banner",
          projectDescription:
            "A poster banner for sporty predict to advertise it's services",
          toolsUsed: {
            adobe: "Adobe Illustrator",
            photoshop: "Photoshop",
          },
        },
        // {
        //   projectType: "Graphic design",
        //   behanceLink:
        //     "https://www.behance.net/",
        //   projectImage:
        //     "https://raw.githubusercontent.com/zero-stealth/portfolio/master/src/assets/poster.png",
        //   projectTitle: "House bistro movie poster",
        //   projectDescription:
        //     "A poster for a movie night event held at house bistro naivasha",
        //   toolsUsed: {
        //     adobe: "Adobe Illustrator",
        //     photoshop: "Photoshop",
        //   },
        // },
      ],
    };
  },
  methods: {
    behanceProject(projectTitle) {
      const project = this.Projects.find((p) => p.projectTitle === projectTitle);
      if (project && project.behanceLink) {
        window.open(project.behanceLink, "_blank");
      }
    },
    githubProject(projectTitle) {
      const project = this.Projects.find((p) => p.projectTitle === projectTitle);
      if (project && project.githubLink) {
        window.open(project.githubLink, "_blank");
      }
    },
    graphicLink(projectTitle) {
      const project = this.Projects.find((p) => p.projectTitle === projectTitle);
      if (project && project.behanceLink) {
        window.open(project.behanceLink, "_blank");
      }
    },
    webLink(projectTitle) {
      const project = this.Projects.find((p) => p.projectTitle === projectTitle);
      if (project && project.projectLink) {
        window.open(project.projectLink, "_blank");
      }
    },
  },
};
</script>

<style>
@import "../style/portfolioView.css";
</style>
