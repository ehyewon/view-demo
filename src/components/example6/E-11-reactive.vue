<template>
  <div>
    <p>Name: {{ person.name }}</p>
    <p>Age: {{ person.age }}</p>
    <button @click="incrementAge">Increment Age</button>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

// 반응형 객체 정의
const person = reactive({
  name: 'John Doe',
  age: 30
})

// 메서드 정의
function incrementAge() {
  person.age++
}
</script>
