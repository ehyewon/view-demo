<template>
  <div>
    <input v-model="id" />
    <input v-model="password" />
    <p>{{ message }}</p>
    <button @click="whoami">whoami</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const id = ref('')
const password = ref('')
const message = ref('Hello Vue')

function whoami() {
  message.value = `${id.value} ${password.value}`
}
</script>
