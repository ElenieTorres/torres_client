<template>
    <div>
        <h1 class="mx-8 border-b-2 border-gray-400 tracking-widest font-medium">CURRENT READS</h1>
    </div>
    <div class="bg-white">
        <div class="mx-auto max-w-7xl overflow-hidden px-4 py-16 sm:px-6 sm:py-10 lg:px-8">
            <div class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 lg:gap-x-8">
                <Cardview v-for="book in cuurent_readsbook" :key="book.id" :href="book.href" 
                :title = "book.title" 
                :author="book.author" 
                :details="book.details" 
                :image-src="book.imageSrc"
                :image-alt="book.imageAlt">
                </Cardview>
            </div>
        </div>
    </div>
</template>
<script setup>
    const cuurent_readsbook = [
    {
        id: 1,
        title: 'NOLI ME TANGERE',
        href: '#',
        author: 'by Dr. JOSE PROTACIO RIZAL MERCADO Y ALONSO REALONDA',
        details: '63 chapters . Nobela , Kasaysayan',
        imageSrc: 'images/book1.jpg',
        imageAlt: '',
    },
    {
        id: 2,
        title: 'TUWAANG AT ANG DILAG NG KALANGITAN NG BUHONG',
        author: 'by E. ARSENIO MANUEL',
        href: '#',
        details: 'Epiko',
        imageSrc: '/images/book4.jpg',
        imageAlt: '',
    },
    {
        id: 3,
        title: 'MARIA CACAO (TRES MARIAS SERYE 2)',
        href: '#',
        author: 'by LISA WONKA',
        details: 'Alamat',
        imageSrc: 'images/book10.jpg',
        imageAlt: '',
    }]
</script>

