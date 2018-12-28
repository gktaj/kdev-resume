<template>
  <div class="c-main-container  js-main-container">
    <Header />
    <Introduction />
    <Expertise />
    <Skills />
    <Experience />
    <Education />
    <Profile />
  </div>
</template>

<script>
import Header from "./Header.vue"
import Introduction from "./Introduction.vue"
import Expertise from "./Expertise.vue"
import Skills from "./Skills.vue"
import Experience from "./Experience.vue"
import Education from "./Education.vue"
import Profile from "./Profile.vue"

export default {
  name: "Main",
  components: {
    Header,
    Introduction,
    Expertise,
    Skills,
    Experience,
    Education,
    Profile
  }
};
</script>
