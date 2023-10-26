<template>
  <header class="bg-blue-500 text-white py-6">
    <div class="container mx-auto flex justify-between items-center">
      <div>
        <NuxtLink to="/" class="text-2xl font-bold border-b-2">SMKN 1 CIOMAS</NuxtLink>
      </div>
      <nav class="flex items-center gap-6">
        <NuxtLink to="/" class="text-lg hover:text-gray-300 hover:border-b-2">Home</NuxtLink>
        <NuxtLink to="/product" class="text-lg hover:text-gray-300 hover:border-b-2">Products</NuxtLink>
        <NuxtLink to="/cart" class="text-lg hover:text-gray-300 hover:border-b-2">Cart</NuxtLink>
      </nav>
    </div>
  </header>
</template>
