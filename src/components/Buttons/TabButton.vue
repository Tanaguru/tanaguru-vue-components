<template>
  <button :class="isActive ? 'btn tabs__btn is-active' : 'btn tabs__btn'">
    {{ content }}
  </button>
</template>

<script>

export default {
  name: 'TabButton',
  props: ['content', 'isActive']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  h3 {
    font-size: 1rem;
    color: black;
  }
</style>
