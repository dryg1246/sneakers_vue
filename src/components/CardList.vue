<script setup>
import Card from "@/components/Card.vue";
</script>

<template>
  <div class="grid grid-cols-5 grid-rows-2 gap-4 ">
    <Card :is-favorite="true" :price="199.99" image-url='/sneakers/sneakers-1.jpg'
          title="Men's Nike Blazer Mid Suede Sneakers"/>
  </div>
</template>