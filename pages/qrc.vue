<script lang="ts" setup>
import { vue3dLoader } from "vue-3d-loader";
</script>



<template>
    <h1 style="font-family:Inconsolata;">please leave my site</h1>
    <vue3dLoader
    src="https://shared-assets.adobe.com/link/19bba73f-c9db-4c6e-663c-1a5668e5f721"
    :height="1000"
    />
</template>


<style>
  @import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200&family=Roboto:wght@100&display=swap');
  body{
    background: black; /* not apply if you go from page-1 to page-2 */
   }
   h1   {color: rgb(72, 235, 72);text-align: center;}
</style>