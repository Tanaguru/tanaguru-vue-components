<template>
  <button class="btn btn--nude btn--icon">
    <icon-base-decorative v-if="hasIconSlot">
      <slot></slot>
    </icon-base-decorative>
    <span>
      {{ content }}
    </span>
  </button>
</template>

<script>
import IconBaseDecorative from '../icons/IconBaseDecorative';
import IconDelete from '../icons/IconDelete';

export default {
  name: 'TextButton',
  components: {
		IconBaseDecorative,
		IconDelete
  },
  props: ['content'],
  computed: {
    hasIconSlot() {
      let condition = false;
      if(this.$slots.default){
        condition = true
      } else { condition = false }
      return condition;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  h3 {
    font-size: 1rem;
    color: black;
  }
</style>
