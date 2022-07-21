<template>
  <div class="gl-layout-wrapper">
    <layout-header/>

    <main class="gl-layout-content-wrapper">
      <main-page/>
    </main>
  </div>
</template>

<script>
import MainPage from "./app/pages/main-page/main-page";
import LayoutHeader from "./app/layout/header/header";

export default {
  name: 'App',
  components: {
    LayoutHeader,
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
