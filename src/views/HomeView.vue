<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
    <HelloVue :msg="'hello Vue3'">
      <template #header>传值给header插槽</template>
    </HelloVue>
  </div>
</template>

<script setup lang="ts">
import HelloWorld from '@/components/HelloWorld.vue' // @ is an alias to /src
import HelloVue from '@/components/HelloVue.vue'
</script>
