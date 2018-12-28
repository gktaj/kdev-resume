<template>
  <div class="c-preloader js-preloader">
    <div class="c-preloader__spinner t-preloader__spinner"></div>
  </div>
</template>

<script>
export default {
  name: "PreLoader",
  props: {
    msg: String
  }
};
</script>
