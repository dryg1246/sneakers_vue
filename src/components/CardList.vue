<script setup>

import Card from "@/components/Card.vue";

defineProps({
  items: Array,
})
</script>

<template>
  <div class="grid grid-cols-5 grid-rows-2 gap-4 ">
    <Card v-for="item in items" :key="item.id" :image-url="item.imageUrl" :price="item.price" :title="item.title"/>
  </div>
</template>