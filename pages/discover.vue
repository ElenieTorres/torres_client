
import Book_overview from '~/components/book_overview.vue';
<template> 
    <div>
        <h1 class="mx-8 border-b-2 border-gray-400 tracking-widest font-medium">NEW IN EPIKO</h1>
        <BookOverview/>
        <CardviewEpiko/>

        <h1 class="mt-10 mb-2 mx-8 border-b-2 border-gray-400 tracking-widest font-medium">MOST READS</h1>
        <CardviewNobela/>
        
        <h1 class="mt-10 mb-2 mx-8 border-b-2 border-gray-400 tracking-widest font-medium">POPULAR IN ALAMAT</h1>
        <CardviewAlamat/>
    </div>
</template>
