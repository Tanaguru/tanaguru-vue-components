<template>
  <button type="button" class="btn btn-pagination btn-pagination--next">
    <icon-base-decorative viewBox="0 0 24 24"><icon-arrow-double /></icon-base-decorative>
    <span class="screen-reader-text">{{ content }}</span>
  </button>
</template>

<script>
import IconBaseDecorative from '../icons/IconBaseDecorative';
import IconArrowDouble from '../icons/IconArrowDouble';

export default {
  name: 'NextPaginationButton',
  components: {
		IconBaseDecorative,
		IconArrowDouble
  },
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
