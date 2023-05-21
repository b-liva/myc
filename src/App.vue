<script setup>
import MButton from './components/libraries/atoms/MButton.vue';
import MInput from './components/libraries/atoms/MInput.vue';
import {ref} from "vue";
let mv = ref()
</script>

<template>
  <main>
    <MButton>{{mv}}</MButton>
    <MInput v-model="mv"/>

  </main>
</template>

<style scoped>

</style>
