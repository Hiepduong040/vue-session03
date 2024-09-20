<template>
  <div>
    <h1>Ex02</h1>
    <p :class="elementClass" :id="elementId">Duong Sy Hiep</p>
  </div>
</template>
  
  <script setup>
const elementClass = "class";
const elementId = "id";
</script>
  
  <style scoped>
.class {
  color: red;
}
#id {
  background-color: cyan;
  width: 100px;
}
</style>