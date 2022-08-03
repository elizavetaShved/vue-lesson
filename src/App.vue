<template>
  <div class="layout-wrapper">
    <main-page/>
  </div>
</template>

<script>
import MainPage from "./pages/main-page/main-page";

export default {
  name: 'App',
  components: {
    MainPage
  }
}
</script>

<style src="./styles/styles.scss" lang="scss"/>
