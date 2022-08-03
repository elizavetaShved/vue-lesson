<template>
  <div class="stories">
    <ul class="stories__wrapper">
      <li
        v-for="(user, index) in usersList"
        :key="index"
        class="stories__item-wrapper"
      >
        <button
          type="button"
          class="stories__item-button"
        >
          <span class="stories__avatar-img-wrapper">
            <img
              :src="user.img"
              :alt="user.name"
              class="stories__avatar-img"
            >
          </span>
          <span class="stories__avatar-name">
            {{ user.name }}
          </span>
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
import { usersList } from "@/pages/main-page/components/stories/usersList";

export default {
  name: 'el-stories',
  data() {
    return {
      usersList: usersList
    }
  }
}
</script>

<style lang="scss" scoped src="./stories.scss"/>
