<template>
    <div class="flex flex-wrap justify-center gap-3 mb-12">
        <button
            v-for="(category, i) in categories"
            :key="i"
            class="px-6 py-2.5 rounded-full font-semibold transition-all"
            :class="{ 'bg-gradient-to-r from-violet-600 to-indigo-600 text-white shadow-lg shadow-violet-500/30': i === 0, 'bg-slate-100 hover:bg-slate-200 text-slate-700': i !== 0 }"
        >
            {{ category }}
        </button>
    </div>
</template>

<script setup lang="ts">
    import { ref } from 'vue';

    const categories = ref<string[]>([
        "All Styles",
        "Cinematic",
        "Minimalist",
        "Vibrant",
        "Retro",
        "Modern",
    ]);
</script>