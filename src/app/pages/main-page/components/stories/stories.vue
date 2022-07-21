<template>
  <div class="list-container">
    <ul class="list-wrapper">
      <li
        v-for="(user, index) in usersList"
        :key="index"
        class="item-wrapper"
      >
        <button type="button" class="item-button">
              <span class="avatar-img-wrapper">
              <img
                :src="user.img"
                :alt="user.name"
                class="avatar-img"
              >
              </span>
          <span class="avatar-name">
                {{ user.name }}
              </span>
        </button>
      </li>
    </ul>
  </div>
</template>

<script>
import { usersList } from "@/app/pages/main-page/components/stories/usersList";

export default {
  name: 'el-stories',
  data() {
    return {
      usersList: usersList
    }
  }
}
</script>

<style lang="scss" scoped>
@import "stories";
</style>
