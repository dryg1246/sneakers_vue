<script setup>

</script>

<template>
  <div class="flex justify-between items-center pt-5 pb-5 ">
    <h2 class="font-bold text-3xl m-4">All sneakers</h2>
    <div class="flex gap-4">
      <div class="relative ">
        <img alt="" class="absolute left-4 top-3" src="/search.svg">
        <input class="border border-slate-200 py-2 pr-4 pl-12 w-full shadow shadow-slate-300"
               placeholder="Search..."
               type="text">
      </div>
      <select class="border border-slate-200 py-2 px-3 shadow shadow-slate-300 outline-0 cursor-pointer ">
        <option value="">Filter</option>
        <option value="">Sort</option>
        <option value="">Search</option>
      </select>
    </div>
  </div>
</template>
