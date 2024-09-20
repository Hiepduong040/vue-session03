<template>
    <div>
      <h1>Ex10</h1>
      <input v-model="text" @keydown="handleKeydown" type="text" />
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const text = ref("");
  
  const handleKeydown = (event) => {
    if (event.key === "Enter") {
      if (event.shiftKey) {
        alert(text.value); 
        text.value = "";     
      } else {
        alert("Bạn cần nhấn Shift + Enter"); 
      }
    }
  };
  </script>
  
  <style>
  </style>
  