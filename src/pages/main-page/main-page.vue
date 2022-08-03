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
import ElStories from "@/pages/main-page/components/stories/stories";
import LayoutHeader from "@/layout/header/header";
import NewsList from "@/pages/main-page/components/news-list/news-list";

export default {
  name: 'main-page',
  components: {
    NewsList,
    LayoutHeader,
    ElStories
  }
}
</script>

<style lang="scss" scoped src="./main-page.scss"/>
