<script setup>
import { onMounted,watch,reactive,ref } from 'vue';
import axios from 'axios';
import Header from './components/Header.vue';
import CardList from './components/CardList.vue';
// import Drawer from './components/Drawer.vue';


const filters = reactive({
  sortBy: 'title',
  searchQuery : ''
})
const items = ref([]);

const onChangeSelect = (event) =>{
  filters.sortBy = event.target.value;
}
const onChangeInput = (event) =>{
    filters.searchQuery = event.target.value;
}
const addToFavorite = async (item) => {
  try {
      item. isFavorite = true;
  }catch(err) {
    console.log(err)
  }
}
const featchFavorites  = async () => {
  try {
    const { data:favorites } = await axios.get (`https://fd8f5ac7362a2e05.mokky.dev/favorites`, {
      
    })
    items.value = items.value.map(item => {
      const favorite = favorites. find(favorite => favorite.perentId === item.id);

      if(!favorite){
        return item;
      }
      return{
        ...item,
        isFavorite: true,
        favoriteId: favorite.id
      }
    })
  }catch(err) {
    console.log(err)
  }
}
const fetchItems = async () => {
try {
  const params = {
    sortBy: filters.sortBy
  }
  if (filters. searchQuery) {
    params.title = `*${filters.searchQuery}*`
  }
  const { data } = await axios.get (`https://fd8f5ac7362a2e05.mokky.dev/items`, {
    params
  })
  items.value = data. map((obj) =>({
    ...obj,
    isFavorite: false,
    isAdded: false
  }))
  } catch (err) {
  console. log (err)
  }
}
onMounted(async ()=>{
  await fetchItems();
  await featchFavorites();
});
watch(filters,fetchItems);
</script>

<template>
  <!-- <Drawer/> -->
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <Header/>
    <div class="p-10 ">
      <div class="flex flex-col  lg:flex-row gap-5 justify-between items-center">

        <h2 class=" text-3xl font-bold ">All sneakers</h2>

        <select @change="onChangeSelect" class="border py-2 pl-2 pr-3 rounded-md outline-none ">
          <option value="name">By name</option>
          <option value="price">By price (cheap)</option>
          <option value="-price">By price (expensive)</option>
        </select>

        <div class="relative" >
          <img class=" absolute left-4 top-3" src="/search.svg" alt="search"/>
          <input 
           @input="onChangeInput" 
          type="text"
          placeholder="Search..."
          class="border rounded-md py-2 pl-11 pr-4 outline-none
          focus:border-gray-400"/>
        </div>
        
      </div>
    </div>
    <div class="mt-10">
      <CardList :items="items"/>
    </div>
  </div>
</template>

