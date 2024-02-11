<script setup>
import Header from './components/Header.vue'
import CardList from "@/components/CardList.vue";
import Search from "@/components/Search.vue";
import {onMounted, reactive, ref, watch} from "vue";
import axios from "axios";

const items = ref([]);
const filters = reactive({
  sortBy: 'title',
  searchQuery: ''
})

const onChangeSelect = (event) => {
  filters.sortBy = event.target.value
}

const onChangeSearch = (event) => {
  filters.searchQuery = event.target.value
}


const fetchItems = async () => {
  try {
    const params = {
      sortBy: filters.sortBy,
    }

    if(filters.searchQuery){
      params.title = `*${filters.searchQuery}*`
    }
    const {data} = await axios.get('https://c9c53c5fefb7365c.mokky.dev/items',
        {
             params
        })
    items.value = data
  } catch (e) {
    console.log(e)
  }
}


onMounted(fetchItems)
watch(filters, fetchItems)


</script>

<template>
  <div class="w-4/5 mx-auto my-10 p-5 bg-white rounded shadow shadow-slate-300">
    <Header/>
    <div class="flex justify-between items-center pt-5 pb-5 ">
      <h2 class="font-bold text-3xl m-4">All sneakers</h2>
      <div class="flex gap-4">
        <div @change="onChangeSearch" class="relative ">
          <img alt="" class="absolute left-4 top-3" src="/search.svg">
          <input  class="border border-slate-200 py-2 pr-4 pl-12 w-full shadow shadow-slate-300"
                 placeholder="Search..."
                 type="text">
        </div>
        <select @change="onChangeSelect" class="border border-slate-200 py-2 px-3 shadow shadow-slate-300 outline-0 cursor-pointer ">
          <option value="title"> alfabet</option>
          <option value="price"> pricing (asc)</option>
          <option value="-price"> pricing (desc)</option>
        </select>
      </div>
    </div>
    <CardList :items="items"/>
    <!--    <Drawer/>-->
  </div>
</template>

