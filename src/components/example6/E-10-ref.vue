<template>
  <div>
    <p>Count: {{ count }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// 반응형 변수 생성
const count = ref(0)

// 함수 정의
function increment() {
  count.value++
}
</script>
