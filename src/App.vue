<template>
  <main>
    <h1>Demo</h1>
    <DemoButtons/>
    <DemoTextField/>
  </main>
</template>

<script>
import DemoButtons from '@/Demos/DemoButtons'
import DemoTextField from "@/Demos/DemoTextField";

export default {
  name: 'App',
  components: {
    DemoTextField,
    DemoButtons,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  html{
    padding: 50px;
  }
</style>