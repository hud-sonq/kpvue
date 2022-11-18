<script lang="ts" setup>
import { vue3dLoader } from "vue-3d-loader";
import { ref } from "vue";
  const rotation = ref();
  rotation.value = {
    x: -Math.PI / 2,
    y: 0,
    z: 0,
  };
  function onLoad() {
    rotate();
  }
  function rotate() {
    requestAnimationFrame(rotate);
    rotation.value.z -= 0.01;
  }
</script>

<template>
    <h1 style="font-family:Inconsolata;">please leave my site</h1>
    <vue3dLoader
    filePath="/scenef/scene.gltf"
    :height="1000"
    :cameraPosition="{ x:10, y:0, z:-10}"
    :backgroundColor="0x000000"
    />
</template>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200&family=Roboto:wght@100&display=swap');
  body{
    background: black; /* not apply if you go from page-1 to page-2 */
   }
   h1   {color: rgb(72, 235, 72);text-align: center;}
</style>