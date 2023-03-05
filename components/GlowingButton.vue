<template>
    <button @click="sayhi"><slot></slot></button>
</template>

<style scoped>
button {
  font-family: Inconsolata;
  width: 250px;
  height: 50px;
  border: none;
  outline: none;
  color: #fff;
  background: #111;
  cursor: pointer;
  position: relative;
  z-index: 0;
  border-radius: 30px;
  margin: 15px;
}


button:before {
  content: '';
  color: #fff;
  background: linear-gradient(45deg, #00eb00, #47ff00, #abffab, #47ff00, #00eb00);
  position: absolute;
  top: -4px;
  left:-4px;
  background-size: 400%;
  z-index: -1;
  filter: blur(5px);
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  animation: glowing 8s linear infinite;
  opacity: 0;
  transition: opacity .3s ease-in-out;
  border-radius: 30px;
}

button:active {
  color: #000;
}

button:active:after {
  transition: 1s;
  background: transparent;
  color: #fff;
}

button:hover:before {
  color: #fff;
  opacity: 1;
}

button:hover:after {
  color: #000;
  opacity: 1;
}

button:after {
  z-index: -1;
  content: '';
  position: absolute;
  width: 0%;
  height: 200%;
  background: #000;
  left: 0;
  top: 0;
  border-radius: 30px;
}

@keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
}
</style>

<script setup>
function sayhi() {
    console.log('smart mf');
}
</script>