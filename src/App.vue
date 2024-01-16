<script setup>
  import MyHelloComponetvuevue from './components/MyHelloComponet.vue'
</script>

<template>
  <div>
    <MyHelloComponetvuevue title="кросоввки Nike" :price="1500" :isAdded="true"/>
    <MyHelloComponetvuevue title="кросоввки Puma" :price="2000" :isAdded="false"/>
  </div>
</template>

<style scoped>

</style>