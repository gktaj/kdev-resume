<template>
  <div class="c-main-container  js-main-container">
    <Header />
    <Introduction />
    <Expertise />
    <Skills />
    <Experience />
    <Education />
    <Profiles />
    <Awards />
    <Portfolio />
    <Clients />
  </div>
</template>

<script>
import Header from "./Header.vue"
import Introduction from "./Introduction.vue"
import Expertise from "./Expertise.vue"
import Skills from "./Skills.vue"
import Experience from "./Experience.vue"
import Education from "./Education.vue"
import Profiles from "./Profiles.vue"
import Awards from "./Awards.vue"
import Portfolio from "./Portfolio.vue"
import Clients from "./Clients.vue"

export default {
  name: "Main",
  components: {
    Header,
    Introduction,
    Expertise,
    Skills,
    Experience,
    Education,
    Profiles,
    Awards,
    Portfolio,
    Clients
  }
};
</script>
