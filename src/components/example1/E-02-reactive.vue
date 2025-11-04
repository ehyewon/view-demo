<!-- example1/E-02-reactive.vue -->
<template>
  <div>{{ fullName }}</div>
</template>

<script setup>
import { ref, computed, onMounted } from 'vue'

// ✅ data() → ref() 로 변환
const firstName = ref('Kyungsu')
const lastName = ref('Lee')

// ✅ computed 속성 변환
const fullName = computed(() => `${firstName.value} ${lastName.value}`)

// ✅ mounted() → onMounted() 훅으로 변경
onMounted(() => {
  console.log('mounted')

  let a = 10

  setTimeout(() => {
    console.log('setTimeout')
    a = 20
    console.log(a)
  }, 500)

  setTimeout(() => {
    lastName.value = '123'
  }, 1000)

  setTimeout(() => {
    firstName.value = 'KSL'
  }, 2000)
})
</script>
