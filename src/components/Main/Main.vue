<template>
  <div class="c-main-container  js-main-container">
    <Header />
    <Introduction />
    <Expertise />
  </div>
</template>

<script>
import Header from "./Header.vue"
import Introduction from "./Introduction.vue"
import Expertise from "./Expertise.vue"

export default {
  name: "Main",
  components: {
    Header,
    Introduction,
    Expertise
  }
};
</script>
