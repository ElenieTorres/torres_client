<template>
    <a :key="id" :href="href" class="group text-sm">
        <div class="aspect-h-1 aspect-w-1 overflow-hidden rounded-lg bg-gray-100 group-hover:opacity-75">
            <img :src="imageSrc" :alt="imageAlt"
                class="h-full w-full object-cover object-center" />
        </div>
        <h3 class="mt-4 font-medium text-base text-gray-900">{{title }}</h3>
        <p class="mt-2 italic text-gray-500">{{ author }}</p>
        <p class="mt-2 font-medium text-gray-900">{{ details }}</p>
    </a>
</template>
  
  <script setup>
    defineProps(['id','href', 'title', 'author', 'details', 'imageSrc', 'imageAlt'])
  </script>