<template>
  <input
      :class="['input', {'input-filled': filled}]" :value="value" @input="onInput">
</template>

<script>
export default {
  name: 'tng-textfield',
  emits: ['input'],
  props: {
    value: null
  },
  methods: {
    onInput(event) {
      this.$emit('input', event.target.value);
    }
  },
  computed: {
    filled() {
      return !!this.value
    }
  }
}
</script>

<style scoped>
input .error{
  border-color: red;
}
</style>