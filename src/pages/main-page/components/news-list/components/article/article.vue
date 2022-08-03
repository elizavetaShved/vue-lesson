<template>
  <div class="news-article">
    <slot name="articleName"></slot>

    <slot name="articleText"></slot>

    <div class="news-article__controls">
      <button type="button" class="news-article__btn news-article__btn--grey news-article__btn--star">
        Star
      </button>

      <button type="button" class="news-article__btn">
        {{ followersNum }}
      </button>

      <button type="button" class="news-article__btn news-article__btn--grey news-article__btn--fork">
        Fork
      </button>

      <button type="button" class="news-article__btn">
        {{ branchNum }}
      </button>
    </div>
  </div>
</template>

<script>


export default {
  name: 'el-article',
  props: {
    followersNum: Number,
    branchNum: Number
  }
}
</script>

<style lang="scss" scoped src="./article.scss"/>
