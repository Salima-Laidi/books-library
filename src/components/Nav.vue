<script setup>
    import { BookOpenText, Plus } from '@lucide/vue';
    import MultiLanguage from "./MultiLanguage.vue";
</script>

<template>
    <nav class="flex justify-between items-start">
        <div class="flex gap-10 items-center">
            <BookOpenText class="text-Dark-brown w-15 h-15" />
            <div>
                <h1 class="text-Dark-brown text-4xl mb-2 font-bold font-headings">My Library</h1>
                <p class="text-Light-beige">A small collection of books</p>
            </div>
        </div>
        <div class="flex gap-4 items-start">
            <MultiLanguage />
            <button class="flex items-center gap-2 bg-Dark-brown py-2 px-4 text-Warm-cream rounded-lg hover:bg-Dark-brown/90 transition-all duration-300 hover:cursor-pointer"><Plus class="w-5 h-5" /> Add Book</button>
        </div>
    </nav>
</template>