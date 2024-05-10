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
        title: 'EL FILIBUSTERISMO',
        href: '#',
        author: 'by Dr. JOSE PROTACIO RIZAL MERCADO Y ALONSO REALONDA',
        details: '39 Chapters . Nobela , Kasaysayan',
        imageSrc: 'images/book3.jpg',
        imageAlt: '',
    },
    {
        id: 2,
        title: 'MGA IBONG MANDARAGIT',
        href: '#',
        author: 'by AMADO V. HERNANDEZ',
        details: '69 Chapters . Nobela , Kasaysayan',
        imageSrc: 'images/book2.jpg',
        imageAlt: '',
    },
    {
        id: 3,
        title: 'NOLI ME TANGERE',
        href: '#',
        author: 'by Dr. JOSE PROTACIO RIZAL MERCADO Y ALONSO REALONDA',
        details: '63 chapters . Nobela , Kasaysayan',
        imageSrc: 'images/book1.jpg',
        imageAlt: '',
    },
    // More books...
  ]
  </script>