<script setup>
import Header from './components/Header.vue';
import CardList from './components/CardList.vue';
// import Drawer from './components/Drawer.vue';

</script>

<template>
  <!-- <Drawer/> -->
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <Header/>
    <div class="p-10 ">
      <div class="flex flex-col  lg:flex-row gap-5 justify-between items-center">

        <h2 class=" text-3xl font-bold ">All sneakers</h2>

        <select class="border py-2 pl-2 pr-3 rounded-md outline-none ">
          <option>By name</option>
          <option>By price (cheap)</option>
          <option>By price (expensive)</option>
        </select>

        <div class="relative" >
          <img class=" absolute left-4 top-3" src="/search.svg" alt="search"/>
          <input type="text"
          placeholder="Search..."
          class="border rounded-md py-2 pl-11 pr-4 outline-none
          focus:border-gray-400"/>
        </div>
        
      </div>
    </div>
    <CardList/>
  </div>
</template>

<style scoped>

</style>