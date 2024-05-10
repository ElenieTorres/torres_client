<template>
    <div class="bg-white">
        <div class="mx-auto max-w-7xl overflow-hidden px-4 py-16 sm:px-6 sm:py-10 lg:px-8">
            <div class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 lg:gap-x-8">
                <a v-for="book in books" :key="book.id" :href="book.href" class="group text-sm">
                    <div class="aspect-h-1 aspect-w-1 overflow-hidden rounded-lg bg-gray-100 group-hover:opacity-75">
                        <img :src="book.imageSrc" :alt="book.imageAlt"
                            class="h-full w-full object-cover object-center" />
                    </div>
                    <h3 class="mt-4 font-medium text-base text-gray-900">{{ book.title }}</h3>
                    <p class="mt-2 italic text-gray-500">{{ book.author }}</p>
                    <p class="mt-2 font-medium text-gray-900">{{ book.details }}</p>
                </a>
            </div>
        </div>
    </div>
  </template>
  
  <script setup>

  const books = [
    {
        id: 1,
        title: 'MARIA SINUKUAN (TRES MARIAS SERYE 1)',
        href: '#',
        author: 'by LISA WONKA',
        details: 'Alamat',
        imageSrc: 'images/book8.jpg',
        imageAlt: '',
    },
    {
        id: 2,
        title: 'MARIA CACAO (TRES MARIAS SERYE 2)',
        href: '#',
        author: 'by LISA WONKA',
        details: 'Alamat',
        imageSrc: 'images/book10.jpg',
        imageAlt: '',
    },
    {
        id: 3,
        title: 'MARIA MAKILING (TRES MARIAS SERYE 3)',
        href: '#',
        author: 'by LISA WONKA',
        details: 'Alamat',
        imageSrc: 'images/book11.jpg',
        imageAlt: '',
    }
    // More books...
  ]
  </script>