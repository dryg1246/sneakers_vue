<script setup>
import DrawerHead from "@/components/DrawerHead.vue";
import CartItemList from "@/components/CartItemList.vue";
import CheckoutButton from "@/components/CheckoutButton.vue";
</script>

<template>
  <div class="fixed top-0 left-0 w-full h-full z-10 bg-black bg-opacity-70 ">
    <div class="w-96 h-full bg-white fixed top-0 right-0 p-5 z-20 p-8">
      <DrawerHead/>
      <CartItemList/>
      <CheckoutButton/>
    </div>
  </div>
</template>