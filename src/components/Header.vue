<template>
     <header class="flex justify-between border-b border-slate-200 px-10 py-8">
      <div class="flex items-center gap-4">
        <img src="/logo.png" alt="Logo" class="w-10"/>
        <div>
          <h2 class="lg:text-xl font-bold uppercase text-center">Vue Sneakers</h2>
          <p class="text-sm lg:text-lg text-slate-300">Collection of products</p>
        </div>
      </div>
      <ul class="hidden  md:flex items-center gap-10 min-w-lg  ">
        <li class="flex items-center gap-2  text-gray-500 hover:text-black cursor-pointer">
          <img src="/cart.svg" alt="cart"/>
          <span>1240 grn</span>
        </li>
        <li class="flex items-center gap-2 text-gray-500 hover:text-black cursor-pointer">
          <img src="/heart.svg" alt="hearts"/>
          <span>Preservation</span>
        </li>
        <li class="flex items-center gap-2  text-gray-500 hover:text-black cursor-pointer">
          <img src="/profile.svg" alt="profile"/>
          <span>Profile</span>
        </li>
      </ul>
    </header>
</template>