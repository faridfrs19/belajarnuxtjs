<!-- Dropdown.vue -->
<template>
    <div class="relative select-none">
      <div
        class="border border-primary flex items-center justify-between px-3 py-2 rounded-lg gap-4 cursor-pointer w-full bg-white"
        @click="isShow = !isShow"
      >
        <span class="text-primary font-medium">Category</span>
        <i
          :class="`ri-arrow-down-s-line text-primary text-xl text-bold transition duration-300 ${isShow ? 'rotate-180' : 'rotate-0'}`"
        ></i>
      </div>
      <!-- Dropdown menu -->
      <div v-show="isShow" class="z-10 bg-white divide-y divide-gray-100 rounded-lg shadow-xl w-full absolute top-14">
        <ul class="py-2 text-sm text-gray-700">
          <li>
            <span
              class="block px-4 py-2 hover:bg-primary hover:text-blue-600 transition duration-200 cursor-pointer bg-gray-200"
              @click="emits('selected-category', '')"
            >
              All
            </span>
          </li>
          <li v-for="(item, index) in props.categories" :key="index">
            <span
              class="block px-4 py-2 hover:bg-primary hover:text-blue-600 transition duration-200 cursor-pointer"
              @click="emits('selected-category', item.name)"
            >
              {{ item?.name }}
            </span>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { ref, defineProps, defineEmits } from 'vue';
  import type { Category } from '~/composables/constants/category';
  
  const isShow = ref(false);
  const props = defineProps<{ categories: readonly Category[] }>();
  const emits = defineEmits(['selected-category']);
  </script>
  
  <style scoped>
  /* Styling for the dropdown button */
  .border-primary {
    border-color: #3498db;
  }
  
  /* Styling for the dropdown menu */
  .bg-gray-200 {
    background-color: #f0f0f0;
  }
  
  /* Styling for hover effect on dropdown items */
  .hover:bg-primary:hover {
    background-color: #3498db;
    color: #fff;
  }
  </style>
  