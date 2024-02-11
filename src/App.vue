<script setup>
import Header from './components/Header.vue'
import CardList from "@/components/CardList.vue";
import Search from "@/components/Search.vue";
import {onMounted, ref} from "vue";
import axios from "axios";

const items = ref([]);
onMounted(async () => {
  try {
    const {data} = await axios.get('https://c9c53c5fefb7365c.mokky.dev/items')
    items.value = data
  } catch (e) {
    console.log(e)
  }
})
</script>

<template>
  <div class="w-4/5 mx-auto my-10 p-5 bg-white rounded shadow shadow-slate-300">
    <Header/>
    <Search/>
    <CardList :items="items"/>
    <!--    <Drawer/>-->
  </div>
</template>

