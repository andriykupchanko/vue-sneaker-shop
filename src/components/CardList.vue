<script setup>
import Card from './Card.vue';
defineProps({
  items:Array
})
</script>
<template>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5">
        <Card  v-for="item in items" 
          :key="item.id"
          :imageUrl="item.imageUrl"
          :title="item.title"
          :price="item.price"
        />
      </div>
      
</template>