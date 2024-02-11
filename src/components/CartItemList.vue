<script setup>
import CartItem from "@/components/CartItem.vue";

const remove = (item) => {
  console.log(item)
}

</script>

<template>
  <div class="flex flex-col gap-4 flex-1 overflow-y-auto justify-between">
    <CartItem :on-click-remove="remove" image-url="/sneakers/sneakers-1.jpg" price="$120"
              title="Men's Nike Blazer Mid Suede Sneakers"/>
  </div>
</template>
