<script setup>
import Header from './components/Header.vue'
import CardList from "@/components/CardList.vue";
</script>

<template>
  <div class="w-4/5 mx-auto my-10 p-5 bg-white rounded shadow shadow-slate-300">
    <Header/>
    <h2 class="font-bold text-3xl m-4">All sneakers</h2>
    <CardList/>
  </div>
</template>

