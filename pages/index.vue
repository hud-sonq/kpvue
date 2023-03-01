<script lang="ts" setup>
import { vue3dLoader } from "vue-3d-loader";
</script>

<template>
<div>
  <vue3dLoader
  filePath="/scenef/scene.gltf"
  :height="200"
  :cameraPosition="{ x:150, y:0, z:-400}"
  :backgroundColor="0x000000"
  />
  <div style="border">
    <h1 style="font-family:Inconsolata;">koipond.xyz is under construction</h1>
    <h2 style="font-family:Inconsolata;">check back in a bit!</h2>
    <h2><MyFancyButton>print money button</MyFancyButton></h2>
  </div>
</div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200&family=Roboto:wght@100&display=swap');
body{
  background: black;
}
a {color:green}
h1 {color: green;text-align: center; font-family: Inconsolata}
h2 {color: green;text-align: center; font-family: Inconsolata}
.containerc {
  max-width: 70%;
  margin: 0 auto;
}
</style>

