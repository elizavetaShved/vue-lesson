<template>
  <layout-header>
    <template v-slot:bottomContent>
      <el-stories/>
    </template>
  </layout-header>

  <main class="layout-content">
    <news-list/>
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
