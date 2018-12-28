<template>
  <div class="home">
    <PreLoader />
    <Main />
  </div>
</template>

<script>
// @ is an alias to /src
import PreLoader from '@/components/PreLoader.vue'
import Main from '@/components/Main/Main.vue'

export default {
  name: 'home',
  components: {
    PreLoader,
    Main,
  }
}
</script>
