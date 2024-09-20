<template>
  <div>
    <h1>Ex03</h1>
    <input v-if="isDisabled" type="text" disabled />
    <input v-else placeholder="Vui long nhap" type="text" />
  </div>
</template>
  
  <script setup>
const isDisabled = true;
</script>
  
  <style>
</style>