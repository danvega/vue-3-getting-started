<template>
  <h1>Hello, Vue 3!</h1>
  <p>{{ count }}</p>
  <button @click="startCounting">Start Counting</button>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const count = ref(0);

    function startCounting() {
      setInterval(() => {
        count.value++
      }, 100);
    }

    return { count, startCounting }
  }
}
</script>
