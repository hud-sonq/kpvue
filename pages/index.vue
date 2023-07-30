<script lang="ts" setup>
import { vue3dLoader } from "vue-3d-loader";

const enablePan = false;
const enableZoom = false;
const enableRotate = false;

const [width, height] = [ref(0), ref(0)];

function reportWindowSize() {
  width.value = window.innerWidth;
  height.value = window.innerHeight;
}
window.onresize = reportWindowSize;
reportWindowSize();

</script>

<template>
  <div class="container">
    
    <div style="overflow: hidden;">
      <vue3dLoader
        filePath="/scenef/scene.gltf"
        :width="width"
        :height="height"
        :cameraPosition="{ x:150, y:900, z:200}"
        :backgroundColor=0
        :scale="{x:1, y:1, z:1}"
        :controlsOptions="{
          enablePan,
          enableZoom,
          enableRotate,
        }"
      />
    </div>
    
    <div class="content">
      <h1>KOIPOND.XYZ is under construction</h1>
      <h2>Check back in a bit!</h2>
      <h2><GlowingButton>Print Money Button</GlowingButton></h2>
    </div>
    
    
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200&family=Roboto:wght@100&display=swap');

body{
  background: black;
  overflow: hidden;
}

a {color:green}
p {color: green}

h1 {
  color: #00c601; 
  text-align: center; 
  font-family: Inconsolata; 
  background-color: transparent;
  overflow: hidden;
}

h2 {
  color: #00c601; 
  text-align: center; 
  font-family: Inconsolata; 
  background-color: transparent;
  overflow: hidden;
}

.containerc {
  max-width: 70%;
  margin: 0 auto;
}

.container {
  display: grid;
  position: relative;
  max-width: 100vw;
  overflow: hidden;
}

.content, .overlay {
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  overflow: hidden;
}
</style>