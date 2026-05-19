<template>
    <div class="bg-gradient-to-br from-slate-900 to-slate-800 py-24 relative overflow-hidden">
        <div class="container mx-auto px-4 relative z-10">
            <div class="text-center mb-16">
                <div class="inline-flex items-center gap-2 bg-white/10 border border-white/20 rounded-full px-5 py-2 mb-6">
                    <LayoutGrid class="w-4 h-4 text-cyan-400" />
                    <span class="text-sm font-semibold text-white">
                        Visual Workspace
                    </span>
                </div>
                <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
                    Your Creative Artboard
                </h2>
                <p class="text-lg text-white/80 max-w-2xl mx-auto">
                    Organize, preview, and refine your AI creations in
                    one intuitive workspace
                </p>
            </div>

            <Filters />
            <Gallery /> 

            <div class="max-w-6xl mx-auto mt-8 text-center">
                <button class="bg-white/10 hover:bg-white/20 backdrop-blur-sm border border-white/20 text-white px-8 py-3 rounded-xl font-semibold transition-all hover:scale-105 inline-flex items-center gap-2">
                    <Sparkles class="w-5 h-5" />
                    Create New Project
                </button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    import { Sparkles, LayoutGrid } from '@lucide/vue';
    import Filters from '../ui/artboard/Filters.vue';
    import Gallery from '../ui/artboard/Gallery.vue';
</script>