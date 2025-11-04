<!-- example1/E-01-instance.vue -->
<template>
  <div>Hello, {{ message }}</div>
</template>

<script setup>
import { ref } from 'vue'

const name = 'hyewon Lee'
const message = ref(name)
</script>

<style scoped>
div {
  color: blue;
}
</style>
