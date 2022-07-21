<template>
  <div class="gl-block-shadow">
    <slot name="articleName"></slot>

    <slot name="articleText"></slot>

    <div class="controls">
      <button type="button" class="btn mod-grey mod-star">
        Star
      </button>

      <button type="button" class="btn">
        {{ followersNum }}
      </button>

      <button type="button" class="btn mod-grey mod-fork">
        Fork
      </button>

      <button type="button" class="btn">
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

<style lang="scss" scoped>
@import "article";
</style>
