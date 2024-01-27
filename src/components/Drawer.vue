<script setup>
    import DrawerHead from './DrawerHead.vue';
    import CardItemList from './CardItemList.vue';
</script>
<template>
    <div class="fixed top-0 left-0 h-full w-full bg-black 
    z-10 opacity-70">
        
    </div>
    <div class="bg-white w-96 h-full fixed  top-0 right-0 
    p-8 z-20"> 
        <DrawerHead/>
        <CardItemList />
        <div class="flex flex-col gap-4 mt-7">
            <div class="flex gap-2 ">
                <span>
                    Total:
                </span>
                <div class="flex-1 border-b border-dashed"></div>
                <b>1200$</b>
            </div>
            <div class="flex gap-2 ">
                <span>
                    Tax:
                </span>
                <div class="flex-1 border-b border-dashed"></div>
                <b>60$</b>
            </div>
            <button class="cursor-pointer bg-lime-500 w-full rounded-xl py-3 
            text-wite transition active:bg-lime-700 hover:bg-lime-600
            disabled:bg-slate-300 mt-7">
                place order
            </button>
        </div>
    </div>
</template>