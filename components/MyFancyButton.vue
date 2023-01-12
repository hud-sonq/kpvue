

<template>
    <button @click="sayhi"><slot></slot></button>
</template>

<style scoped>
button {
  height: 50px;
  width: 200px;
  border-radius: 0;
  border-width: 0;
  background-color: green;
  color: black;
  font-family: Inconsolata;
}
</style>

<script setup>
function sayhi() {
    console.log('smart mf');
}
</script>