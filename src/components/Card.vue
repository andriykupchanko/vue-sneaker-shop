<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isFavorit:Boolean,
  isAdded:Boolean,
  onClickAdd:Function,
  onClickFavorite:Function
})
</script>
<template>
    <div>
        <div>
      <div class="bg-white relative border border-slate-100 rounded-3xl p-8 cursor-pointer transition hover:-translate-y-2 hover:shadow-xl">
        <img @oncliclk="onClickFavorite" :src="isFavorit ? '/like-2.svg' : '/like-1.svg'" alt="like 1" class="absolute top-8 left-8"/>
        <img :src="imageUrl" alt="sneakers"/>
        <p class="mt-2">{{ title }}</p>
        <div class="flex justify-between">
          <div class="flex flex-col mt-5">
            <span class="text-slate-400">Price:</span>
            <b>{{ price }}$</b>
          </div>
          <img @oncliclk="onClickAdd" :src="isAddet ? '/checked.svg' : '/plus.svg'" alt="plus"/>
        </div>
      </div>
    </div>
    </div>
</template>