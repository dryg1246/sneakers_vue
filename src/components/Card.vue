<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function,
  id: Number
})
</script>

<template>
  <div>
    <div
        class="border border-black p-2 w-52 h-72 m-4 rounded-xl border-opacity-5 hover: -translate-y-2 hover:shadow-2xl transition duration-300 ease-in cursor-pointer ">
      <div class="flex justify-center">
        <img :src="imageUrl" alt="" class="w-36 h-36 ">
        <img :src="isFavorite ? '/like-2.svg' : '/like-1.svg'" alt="" class="relative -top-10 right-36 "
             @click="onClickFavorite">
      </div>
      <div>
        <h3 class="text-center  font-bold text-gray-700 mt-2 ">{{ title }}</h3>
      </div>
      <div class="flex justify-between ">
        <div class="flex flex-col mt-2  ml-4">
          <span class="  opacity-20">price: </span>
          <b class="font-bold">{{ price }} $</b>
        </div>
        <img :src="!isAdded ? '/plus.svg' : '/checked.svg'" alt="" class=" mt-2" @click="onClickAdd">
      </div>
    </div>
  </div>
</template>
