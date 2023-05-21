<script setup>
import {computed, ref} from "vue";
const props = defineProps(['modelValue'])
const emit = defineEmits(['update:modelValue'])
let modelValue = ref()
const computedValue = computed({
  get() {
    return props.modelValue
  },
  set(newValue){
    emit('update:modelValue', newValue)
  }
})
</script>

<template>
  <input class="m-input" v-bind="$attrs" v-model="computedValue" />
</template>

<style lang="scss">
.m-input {
  display: block;
  width: 100%;
  border: 1px solid #eee;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  margin: 0.2rem 0;
  box-sizing: border-box;

  &:focus {
    outline: none;
    box-shadow: 0 0 0 3px rgba(#40b983, 0.2);
  }
}
</style>