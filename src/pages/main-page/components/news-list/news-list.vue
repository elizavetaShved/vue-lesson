<template>
  <div class="news-list">
    <div class="news-list__content-wrapper">
      <ul class="news-list">
        <li
          v-for="(news, index) in newsList"
          :key="index"
          class="news-list__item-wrapper"
        >
          <user-link :user="news.user"/>

          <el-article :followersNum="news.followersNum" :branchNum="news.branchNum">
            <!-- тут slot не оч уместен, но в задании нужно сделать слотом-->
            <template v-slot:articleName>
              <div class="news-list__article-title">
                {{ news.articleName }}
              </div>
            </template>
            <template v-slot:articleText>
              <div v-html="news.articleText" class="news-list__article-text"/>
            </template>
          </el-article>

          <div class="news-list__issues-wrapper">
            <el-toggler :isOpen="togglerOpenIndex[index]" @on-click="onChangeStatusToggler(index)"/>

            <ul
              class="news-list__issues-list"
              :class="{'mod-show': togglerOpenIndex[index]}"
            >
              <li
                v-for="(issue, index) in news.issuesList"
                :key="index"
                class="news-list__issues-item"
              >
                <a :href="issue.user.link" class="news-list__issues-name-link">
                  {{ issue.user.name }}
                </a>
                <div class="news-list__issues-text">
                  {{ issue.issues }}
                </div>
              </li>
            </ul>
          </div>

          <div class="news-list__date">
            {{ parsDate(news.date) }}
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>

import { newsListData } from "@/pages/main-page/components/news-list/news-list-data.js";
import UserLink from "@/pages/main-page/components/news-list/components/user-link/user-link";
import ElArticle from "@/pages/main-page/components/news-list/components/article/article";
import ElToggler from "@/pages/main-page/components/news-list/components/toggler/toggler";

export default {
  name: 'news-list',
  components: {
    ElToggler,
    ElArticle,
    UserLink
  },
  data() {
    return {
      // fixme данные с API-запроса
      newsList: newsListData,
      togglerOpenIndex: []
    }
  },
  methods: {
    onChangeStatusToggler(index) {
      this.togglerOpenIndex[index] = !this.togglerOpenIndex[index];
    },
    parsDate(dateStr) {
      let ms = new Date(dateStr).getTime();
      let date = new Date(ms);
      return date.toLocaleDateString("en-GB", { day: 'numeric', month: 'long' });
    }
  },
  mounted() {
    this.togglerOpenIndex = new Array(this.newsList.length).fill(false);
  }
}
</script>

<style lang="scss" scoped src="./news-list.scss"/>
