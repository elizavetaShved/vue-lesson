<template>
  <header class="header">
    <div class="gl-page-content">
      <div class="content">
        <a href="/" class="logo-link"/>

        <div class="controls-wrapper">
          <a href="" class="link link-home"/>

          <a href="" class="link link-account">
            <img :src="avatarImg" alt="account" class="link-account-image">
          </a>

          <a class="link link-exit"/>
        </div>
      </div>

      <slot name="bottomContent"></slot>
    </div>
  </header>
</template>

<script>
export default {
  name: 'layout-header',
  data() {
    return {
      // fixme тут, вероятно, юзера из API запроса получим, и заберем img
      avatarImg: "img/avatar-11.png"
    }
  }
}
</script>

<style lang="scss" scoped>
@import "header";
</style>
