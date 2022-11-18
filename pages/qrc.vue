<script lang="ts" setup>
import { vue3dLoader } from "vue-3d-loader";
</script>

<template>
    <h1 style="font-family:Inconsolata;">please leave my site</h1>
    <vue3dLoader
    filePath="/models/tinker.obj"
    :cameraPosition="{ x: 1, y: -5, z: -20 }"
    :height="350"
    />
</template>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200&family=Roboto:wght@100&display=swap');
  body{
    background: black; /* not apply if you go from page-1 to page-2 */
   }
   h1   {color: rgb(72, 235, 72);text-align: center;}
</style>