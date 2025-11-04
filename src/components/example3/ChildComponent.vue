<script setup>
import { defineProps, defineEmits } from 'vue'

// props 전체를 객체로 받기
const props = defineProps({
  message: String,
  id: Number,
  password: Number,
})

const emit = defineEmits(['custom-event'])

function sendEvent() {
  emit('custom-event', 'Hello from child')
}
</script>

<template>
  <div>
    <p>{{ props.message }}</p>
    <p>{{ props.id }}</p>
    <p>{{ props.password }}</p>
    <button @click="sendEvent">Send Event</button>
  </div>
</template>
