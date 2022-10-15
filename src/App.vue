<template>
  <p>
    <button @click="increase">count:{{ countRef }}</button>
  </p>
</template>
<script>
import { ref } from 'vue'

function useCount() {
  let countRef = ref(0);
  const increase = () => {
    countRef.value++;
  }
  return {
    countRef,
    increase
  }
}

export default {
  setup() {
    return {
      ...useCount()
    }
  }
}
</script>
