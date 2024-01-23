<script setup>
    import DrawerHead from './DrawerHead.vue';
    import CardItemList from './CardItemList.vue';
</script>
<template>
    <div class="fixed top-0 left-0 h-full w-full bg-black 
    z-10 opacity-70">
        
    </div>
    <div class="bg-white w-96 h-full fixed top-0 right-0 
    p-8 z-20"> 
        <DrawerHead/>
        <CardItemList/>
        <div>
            <div>
                <span>

                </span>
            </div>
        </div>
    </div>
</template>