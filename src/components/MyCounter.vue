<template>
  <div>
    <h3>MyCounter component</h3>
    Reactive variable count: <b>{{ count }}</b>
    <p>
      <button @click="count++">Increment</button>
      <button @click="count--">Decrement</button>
    </p>
  </div>
</template>
<script setup>
import { ref } from 'vue';

const count = ref(0);
</script>
<style scoped>
p {
  font-family: papyrus;
  font-size: 20px;
}

.red-text {
  color: red;
}
</style>
