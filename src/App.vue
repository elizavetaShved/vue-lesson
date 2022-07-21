<template>
  <div class="gl-layout-wrapper">
    <main-page/>
  </div>
</template>

<script>
import MainPage from "./app/pages/main-page/main-page";

export default {
  name: 'App',
  components: {
    MainPage
  }
}
</script>

<style lang="scss">
@import "src/app/common/styles/reset.scss";
@import "src/app/common/styles/fontface.scss";
@import "src/app/common/styles/consts.scss";
@import "src/app/common/styles/global.scss";
</style>
