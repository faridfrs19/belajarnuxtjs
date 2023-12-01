<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
    product: {
        type: Object,
        default: {},
    },
});
</script>

<template>
    <section class="py-10">
        <div class="container">
            <NuxtLink to="/product"
                class="bg-white border border-slate-300  hover:bg-blue-800  hover:text-white w-max flex items-center gap-1 py-2 px-5 rounded-full mb-7 cursor-pointer">
                <i class="ri-arrow-left-s-line text-base font-medium"></i>
                <span class="text-base font-medium">Kembali</span>
            </NuxtLink>
        </div>
    </section>
</template>
