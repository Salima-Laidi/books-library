<script setup>
    import { Globe, ChevronDown, ChevronUp } from '@lucide/vue';
    import {ref} from "vue";
    const languages = ["EN", "FR"];
    const selected = ref(languages[0]);
    const open = ref(false);
</script>

<template>
    <div>
        <button class="flex items-center gap-2 text-Dark-brown py-2 px-3 border border-Dark-brown/50 rounded-lg hover:border-Dark-brown hover:cursor-pointer transition-all duration-30" @click="open = !open">
            <Globe class="w-5 h-5" /> 
            {{ selected }} 
            <ChevronDown class="w-5 h-5" v-if="!open" />
            <ChevronUp class="w-5 h-5" v-else />
        </button>
        <div class="bg-Off-white z-40 w-full flex flex-col gap-2 p-3 mt-2 rounded-lg  text-Dark-brown" v-if="open">
            <button v-for="(language,index) in languages" :key="index" class="hover:bg-Dark-brown/10 hover:cursor-pointer transition-all duration-300 rounded-md" :class="selected === language && `bg-Dark-brown/10`" @click="selected = language; open = false;" >{{ language }}</button> 
        </div>
    </div>
</template>