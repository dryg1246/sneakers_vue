<script setup>

</script>

<template>
  <div class="flex flex-col gap-4 mt-7">
    <div class="flex justify-between  gap-3">
      <p>Итого: </p>
      <div class="border-dashed flex-1 border-b "></div>
      <b>120$</b>
    </div>
    <div class="flex justify-between gap-3">
      <p>Доставка: </p>
      <div class="border-dashed flex-1 border-b "></div>
      <b>120$</b>
    </div>
    <button
        class=" mt-4 bg-lime-400 w-full  justify-center cursor-pointer text-white p-3 rounded-xl disabled:bg-slate-400 flex gap-3 transition-all duration-300 items-center  text-lg hover:bg-lime-600  active:bg-lime-700"
        disabled="">
      <p>Order </p>
      <img alt="" src="/arrow-right.svg">
    </button>
  </div>
</template>
