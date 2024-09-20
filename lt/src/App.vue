<template>

  <div>
    <p v-if="isVIf">hiển thị nếu ddkien V-If thỏa mãn</p>
    <p>V-show</p>
    <p v-show="isVShow"> hiển thị nếu ddkien V-show thỏa mãn</p>
    <ul>
      <li v-if="age>30">Tuổi trung niên</li>
      <li v-else-if="age>18">Tuổi thanh niên</li>
      <li v-else-if="age>6">Tuổi trưởng thành</li>
      <li v-else> trẻ nhỏ</li>
    </ul>
    <p>***************************************</p>
    <p>v-for: hiển thị dữ liệu về mảng</p>
    <ul>
      <li v-for="(student,index) in students " :key="student.id">{{index + 1}} {{student.name}}</li>
    </ul>
    <p>******************************</p>
    <p>V-model</p>

    <div>
      <input :value="inputText"  type="text" @input="handleChange">
      <p>giá trị bạn nhập:{{inputText}}</p>
    </div>
    <div>
      <p>Bài tập 11</p>
      <p>Count: {{count}}</p>
      <button  @click="increase">tĂNG</button>
    </div>
    <p>*****************</p>
    <p>event</p>
    <button @click="handleClick('hello')">button</button>
  </div>

</template>

<script setup>
  import { ref } from "vue";
  const isVIf= false;
  const isVShow = true;
  const age=30;
  const students=[
    {
      id:1,
      name:"Hồng Vân"
    },
    {
      id:2,
      name:"Ánh Linh"
    },
    {
      id:3,
      name:"Thảo Phương"
    },
  ]
  const count = ref(0);
  const inputText=ref("hello");
  const handleChange=(event)=>{
    console.log("da goi vao ham",event.target.value);
    inputText.value = event.target.value
  }
  const increase=()=>{
    console.log("da goi ham!",count);
    count.value = count.value+1;
    
  }
  const handleClick=(mess)=>{
    console.log("gia tri nhan ve,", mess);
    
  }

</script>

<style>

</style>