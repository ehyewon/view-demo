<template>
  <div>
    <input ref="inputField" type="text" placeholder="Click the button to focus" />
    <button @click="focusInput">Focus Input</button>
  </div>
</template>

<script setup>
import {
  ref,
  onMounted,
  onBeforeMount,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted
} from 'vue'

// DOM 요소 참조
const inputField = ref<HTMLInputElement | null>(null)

// 포커스 함수
function focusInput() {
  inputField.value?.focus()
}

// 라이프사이클 훅들
onBeforeMount(() => console.log('beforeMount', inputField))
onMounted(() => {
  console.log('mounted', inputField)
  inputField.value?.focus()
})
onBeforeUpdate(() => console.log('beforeUpdate', inputField))
onUpdated(() => console.log('updated', inputField))
onBeforeUnmount(() => console.log('beforeUnmount', inputField))
onUnmounted(() => console.log('unmounted', inputField))
</script>
