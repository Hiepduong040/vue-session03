<template>
  <div>
    <h1>Ex09</h1>
    <button @click="handleClick()">Count {{ count }}</button>
  </div>
</template>
    
    <script setup>
import { ref } from "vue";
const count = ref(0);
const handleClick = () => {
  count.value++;
};
</script>
    
    <style>
</style>