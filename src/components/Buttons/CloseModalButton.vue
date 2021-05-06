<template>
  <button type="button" class="btn btn--nude btn--icon" :aria-label="ariaLabel">
    <icon-base-decorative width="18" height="18"><icon-close /></icon-base-decorative>
    <span>{{ content }}</span>
  </button>
</template>

<script>
import IconBaseDecorative from '../icons/IconBaseDecorative';
import IconClose from '../icons/IconClose';

export default {
  name: 'CloseModalButton',
   components: {
		IconBaseDecorative,
		IconClose
  },
  props: ['content', 'ariaLabel']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  #buttons {
		width: 30%;
		margin: auto;
		display: flex;
		justify-content: space-around;
	}

  h3 {
    font-size: 1rem;
    color: black;
  }
</style>
