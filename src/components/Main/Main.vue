<template>
  <div class="c-main-container  js-main-container">
    <Header />
    <Introduction />
  </div>
</template>

<script>
import Header from "./Header.vue"
import Introduction from "./Introduction.vue"

export default {
  name: "Main",
  components: {
    Header,
    Introduction
  }
};
</script>
