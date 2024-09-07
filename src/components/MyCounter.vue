<template>
  <div>
    <h3>MyCounter component</h3>
    Reactive variable count: <b>{{ count }}</b> <br />Double count:
    <b>{{ doubleCount }}</b>
    <p>
      <button @click="increment()">Increment</button>
      <button @click="decrement()">Decrement</button>
    </p>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const count = ref(0);
const doubleCount = computed(() => {
  return count.value * 2;
});

const increment = () => {
  count.value++;
};

const decrement = () => {
  count.value--;
};
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
