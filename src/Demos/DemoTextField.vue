<template>
  <section>
    <h2>Text fields</h2>

    <h3>Text</h3>
    <tng-textfield value="a text"/>

    <h3>Text invalid</h3>
    <tng-textfield class="invalid" value="a text"/>

    <h3>Text valid</h3>
    <tng-textfield class="valid" value="a text"/>
  </section>
</template>

<script>
import TngTextfield from "@/components/Inputs/TngTextfield";
export default {
  components: {TngTextfield}
}
</script>