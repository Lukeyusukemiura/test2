<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HeaderAll from "@/components/HeaderAll.vue";
</script>

<template>
  <HeaderAll />
   <body class="box sm:bg-yellow-500">Hello this is an home page
  </body>
</template>

<style>
.box{
  height: 100vh;
  width: 100%;
}
</style>
