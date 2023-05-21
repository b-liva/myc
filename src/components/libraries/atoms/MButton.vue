<script setup>

</script>

<template>
  <button class="m-button" v-bind="$attrs">
    <slot />
  </button>
</template>

<style>
.m-button {
  background-color: #40b983; /* Green */
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 1rem;
}
</style>