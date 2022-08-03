<template>
  <a
    :href="user.link"
    class="news-user"
  >
    <img
      :src="user.img"
      :alt="user.name"
      class="news-user__img"
    >
    <div class="news-user__name">
      {{ user.name }}
    </div>
  </a>
</template>

<script>


export default {
  name: 'user-link',
  props: {
    user: {
      name: String,
      img: String,
      link: String
    }
  }
}
</script>

<style lang="scss" scoped src="./user-link.scss"/>
