<template>
  <div id="app">
    <PreLoader />
    <Main />
  </div>
</template>

<script>
import PreLoader from "@/components/PreLoader.vue"
import Main from "@/components/Main.vue"

export default {
  name: "app",
  components: {
    PreLoader,
    Main
  }
};
</script>
