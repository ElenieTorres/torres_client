<template>
    <div>
        <h1 class="mx-8 border-b-2 border-gray-400 tracking-widest font-medium">NEW UPLOADS</h1>
    </div>
    <div class="bg-white">
        <div class="mx-auto max-w-7xl overflow-hidden px-4 pt-16 sm:px-6 sm:py-10 lg:px-8">
            <div class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 lg:gap-x-8">
                <Cardview v-for="book in booklist_update" :key="book.id" :href="book.href" 
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
    const booklist_update = [
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
    },
    {
        id: 4,
        title: 'AMBURUKAY: SUGIDANON (EPICS) OF PANAY BOOK 2',
        href: '#',
        author: 'by FEDERICO “TUOHAN” CABALLERO, LEOPOLDO “PAINO” CABALLERO, and ALICIA P. MAGOS',
        details: 'Epiko',
        imageSrc: 'images/book5.jpg',
        imageAlt: '',
    },
    {
        id: 5,
        title: 'SINAGNAYAN: SUGIDANON (EPICS) OF PANAY BOOK 6',
        href: '#',
        author: 'by MAGOS, ALICIA P. & RAMIREZ, ANNA RAZEL LIMOSO',
        details: 'Epiko',
        imageSrc: 'images/book7.png',
        imageAlt: '',
    },
    {
        id: 6,
        title: 'BALANAKON: SUGIDANON (EPICS) OF PANAY BOOK 7',
        href: '#',
        author: 'by MAGOS, ALICIA P. & RAMIREZ, ANNA RAZEL LIMOSO',
        details: 'Epiko',
        imageSrc: 'images/book6.jpg',
        imageAlt: '',
    },
    ]
</script>


