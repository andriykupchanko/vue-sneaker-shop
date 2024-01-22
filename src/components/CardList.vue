<script setup>
import Card from './Card.vue';
</script>
<template>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-5">
        <Card imageUrl="/sneakers/sneakers-1.jpg" title="Men Sneakers Nike Blaser Mid Suede" :price="400" :isAddet="true"/>
      </div>
      
</template>