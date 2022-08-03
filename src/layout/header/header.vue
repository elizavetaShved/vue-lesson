<template>
  <header class="header">
    <div class="header__content-wrapper">
      <div class="header__content">
        <a href="/" class="header__logo-link"/>

        <div class="header__controls-wrapper">
          <a href="" class="header__link header__link--home"/>

          <a href="" class="header__link header__link--account">
            <img :src="avatarImg" alt="account" class="header__link-image">
          </a>

          <a class="header__link header__link--exit"/>
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

<style lang="scss" scoped src="./header.scss"/>
