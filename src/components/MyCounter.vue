<template>
  <div>
    <h3>MyCounter component</h3>
    Reactive variable count: <b>{{ count }}</b> <br />Double count:
    <b>{{ doubleCount }}</b>
    <p>
      <button @click="increment()">Increment</button>
      <button @click="decrement()">Decrement</button>
      <button @click="startCount()">Start</button>
      <button @click="stopCount()">Stop</button>
    </p>
  </div>
</template>

<script setup>
import {
  ref,
  computed,
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted,
} from 'vue';

console.log('setup: The component is created in memory.');

let timer;
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

const startCount = () => {
  timer = setInterval(() => {
    increment();
  }, 1000);
};

const stopCount = () => {
  clearInterval(timer);
};

onBeforeMount(() => {
  console.log('onBeforeMount: The component is to be mounted in DOM.');
});

onMounted(() => {
  console.log('onMounted: The component is mounted in DOM.');
  startCount();
});

onBeforeUpdate(() => {
  console.log('onBeforeUpdate: The component is to be updated in DOM.');
});

onUpdated(() => {
  console.log('onUpdated: The component is updated in DOM.');
});

onBeforeUnmount(() => {
  console.log('onBeforeUnmount: The component is to be unmounted in DOM.');
});

onUnmounted(() => {
  console.log('onUnmounted: The component is unmounted in DOM.');
  stopCount();
});
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
