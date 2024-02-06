<script setup>
import Templating from './components/Templateing.vue';
import TextAreaField from './components/TextAreaField.vue';
</script>

<template>
  lort med lort på
  <hr>
  <Templating />
  <hr class="bigLine">
  <h1>OPG 1</h1>
  <TextAreaField />
  <hr class="bigLine">
  <h1>OPG 2</h1>
</template>

<style lang= "scss" scoped>


.bigLine{
  background-color: black;
  height: 25px;
  width: 100%;
}

</style>
