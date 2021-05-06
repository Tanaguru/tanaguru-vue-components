<template>
  <button
    type="button"
    :class="firstToLast ? 'btn btn--default-inverse btn--icon' : 'btn btn--default btn--icon'"
    :aria-pressed="pressed"
  >
    {{ content }}
    <icon-base-decorative v-if="firstToLast">
        <icon-close/>
    </icon-base-decorative>

    <icon-base-decorative v-else>
        <icon-checked/>
    </icon-base-decorative>
  </button>
</template>

<script>
import IconBaseDecorative from '../icons/IconBaseDecorative';
import IconClose from '../icons/IconClose';
import IconChecked from '../icons/IconChecked';

export default {
  name: 'SortButton',
  components: {
    IconBaseDecorative,
    IconClose,
    IconChecked
  },
  props: ['content', 'firstToLast', 'pressed']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  h3 {
    font-size: 1rem;
    color: black;
  }
</style>
