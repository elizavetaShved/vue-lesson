<template>
  <button
    type="button"
    class="toggler"
    :class="{'mod-show': isOpen}"
    @click="onClickToggler"
  >
    {{ isOpen ? "Hide issues" : "View issues" }}
  </button>
</template>

<script>


export default {
  name: 'el-toggler',
  emits: ['on-click'],
  props: {
    isOpen: Boolean
  },
  methods: {
    onClickToggler() {
      this.$emit('on-click');
    }
  }
}
</script>

<style lang="scss" scoped>
@import "toggler";
</style>
