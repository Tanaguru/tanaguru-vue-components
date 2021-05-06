<template>
  <button
    :class="burgerOpen ? 'btn btn--nude btn-menu is-active' : 'btn btn--nude btn-menu'"
    :aria-expanded="burgerOpen"
    :aria-controls="pannelId"
  >
  	<span v-if="burgerOpen">{{ openContent }}</span>
    <span v-else>{{ closedContent }}</span>
    <span aria-hidden="true" class="toggle">
      <span class="toggle__bar toggle__bar--top"></span>
      <span class="toggle__bar toggle__bar--middle"></span>
      <span class="toggle__bar toggle__bar--bottom"></span>
    </span>
  </button>
</template>

<script>

export default {
  name: 'MenuButton',
  props: ['openContent', 'closedContent', 'burgerOpen', 'pannelId'],
  created(){
    console.log(this.burgerOpen)
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .btn-menu {
    color: $text-primary;
    text-transform: uppercase;

    > span {
      vertical-align: middle;
    }

    &.is-active {
      .toggle {
        .toggle__bar {
          &.toggle__bar--top {
            top: 50%;
            transform: rotate(45deg) translateY(-50%);
          }

          &.toggle__bar--middle {
            opacity: 0;
          }

          &.toggle__bar--bottom {
            bottom: 50%;
            transform: rotate(-45deg) translateY(50%);
          }
        }
      }
    }
  }

  // Toggle burger menu
  .toggle {
    position: relative;
    display: inline-block;
    margin-left: 1rem;
    width: 2.8rem;
    height: 2.2rem;

    .toggle__bar {
      position: absolute;
      right: 0;
      left: 0;
      display: block;
      width: 2.8rem;
      height: .2rem;
      transform-origin: center;
      transition: transform .3s ease-out, opacity .3s ease-out;
      background-color: $text-secondary;

      &.toggle__bar--top {
        top: 0;
      }

      &.toggle__bar--middle {
        top: 50%;
        transform: translateY(-50%);
      }

      &.toggle__bar--bottom {
        bottom: 0;
      }
    }
  }
</style>
