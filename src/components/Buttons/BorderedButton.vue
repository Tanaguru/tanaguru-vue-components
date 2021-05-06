<template>
  <button type="button" class="btn btn--default btn--icon">
		<icon-base-decorative width="18" height="18" v-if="hasIconSlot">
      <slot></slot>
    </icon-base-decorative>
    <span>{{ content }}</span>
  </button>
</template>

<script>
import IconBaseDecorative from '../icons/IconBaseDecorative';

export default {
  name: 'BorderedButton',
  components: {
		IconBaseDecorative
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
