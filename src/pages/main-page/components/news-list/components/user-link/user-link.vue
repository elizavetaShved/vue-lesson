<template>
  <a
    :href="user.link"
    class="user-link"
  >
    <img
      :src="user.img"
      :alt="user.name"
      class="user-img"
    >
    <div class="user-name">
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
