<template>
  <button
    type="button"
    class="news-toggler"
    :class="{'news-toggler--show': isOpen}"
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

<style lang="scss" scoped src="./toggler.scss"/>
