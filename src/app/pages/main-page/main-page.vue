<template>
  <layout-header>
    <template v-slot:bottomContent>
      <el-stories/>
    </template>
  </layout-header>


  <main class="gl-layout-content-wrapper">
    <div class="container">
      <news-list/>
    </div>
  </main>
</template>

<script>
import ElStories from "@/app/pages/main-page/components/stories/stories";
import LayoutHeader from "@/app/layout/header/header";
import NewsList from "@/app/pages/main-page/components/news-list/news-list";

export default {
  name: 'main-page',
  components: {
    NewsList,
    LayoutHeader,
    ElStories
  }
}
</script>

<style lang="scss" scoped>
@import "main-page";
</style>
