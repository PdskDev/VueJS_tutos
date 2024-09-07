<template>
  <h1>MyCounter {{ message }}</h1>
</template>
<script>
export default {
  name: 'MyCounter',
  props: {
    message: String,
  },
};
</script>
<style scoped></style>
