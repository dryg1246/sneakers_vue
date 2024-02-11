<script setup>
defineProps({
  title: String,
  price: Number,
  imageUrl: String,
  onClickRemove: Function,
})
</script>

<template>
  <div class="flex items-center justify-between border border-slate-100 p-4 rounded-2xl mt-4">
    <div class="flex gap-4">
      <img :src="imageUrl" alt="" class="w-16 h-16">
      <div class="flex flex-col justify-between ">
        <p class="">{{ title }}</p>
        <div class="flex justify-between">
          <b>{{ price }}</b>
          <img alt="" class=" opacity-40 cursor-pointer hover:opacity-100 transition" src="/close.svg"
               @click="onClickRemove">
        </div>
      </div>
    </div>
  </div>
</template>
