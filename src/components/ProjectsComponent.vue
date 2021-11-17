<template>
  <div class="portfolio">
    <div class="row">
      <project-component
        :project="projects.pma"
        :class="{ 'slide-left': loading }"
      >
      </project-component>

      <project-component
        :project="projects.paint"
        :class="{ 'slide-right': loading }"
      >
      </project-component>
    </div>

    <div class="row">
      <project-component
        :project="projects.unityARPG"
        :class="{ 'slide-left': loading }"
      >
      </project-component>

      <project-component
        :project="projects.visiFood"
        :class="{ 'slide-right': loading }"
      >
      </project-component>
    </div>

    <div class="row">
      <project-component
        :project="projects.unityLights"
        :class="{ 'slide-left': loading }"
      >
      </project-component>

      <project-component
        :project="projects.speedometer"
        :class="{ 'slide-right': loading }"
      >
      </project-component>
    </div>
    <div class="row">
      <project-component
        :project="projects.portfolio"
        :class="{ 'slide-left': loading }"
      >
      </project-component>
    </div>
  </div>
</template>

<script>
import ProjectComponent from "../components/ProjectComponent";

export default {
  components: { ProjectComponent },
  data() {
    return {
      loading: true,
      projects: {
        pma: {
          name: "Spring Project Management",
          summary:
            "A project management web app build with Andriod Studio. Users can enter chatrooms with other students to discuss classes before enrollment. \n T",
          img: "spring.png",
          code: "https://github.com/jkonyan25/project-management",
          technologies: [
            { name: "Java" },
            { name: "Android Studio" },
            { name: "HTML" },
           
        
            //{name: 'REST API with Swagger'},
          ],
        },

        
      },
    };
  },
  mounted() {
    setTimeout(() => {
      this.loading = false;
    }, 400);
  },
};
</script>

<style lang="scss">
.portfolio {
  margin-top: 4rem;
}

.slide-left {
  opacity: 0;
  visibility: hidden;
  transform: translateX(-5rem);
}
.slide-right {
  opacity: 0;
  visibility: hidden;
  transform: translateX(5rem);
}
</style>