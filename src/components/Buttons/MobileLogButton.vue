<template>
  <button class="btn btn--nude btn--logout">
    {{ content }}
  </button>
</template>

<script>

export default {
  name: 'MobileLogButton',
  props: ['content']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  h3 {
    font-size: 1rem;
    color: black;
  }
</style>
