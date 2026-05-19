<template>
    <div class="bg-white py-24">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <div class="inline-flex items-center gap-2 bg-violet-100 border border-violet-200 rounded-full px-5 py-2 mb-6">
                    <Palette class="w-4 h-4 text-violet-600" />
                    <span class="text-sm font-semibold text-violet-700">
                        AI Style Library
                    </span>
                </div>
                <h2 class="text-4xl md:text-5xl font-bold text-slate-900 mb-4">
                    Explore Thousands of Styles
                </h2>
                <p class="text-lg text-slate-600 max-w-2xl mx-auto">
                    Browse our curated collection of AI styles and
                    presets. Click any style to preview and apply
                </p>
            </div>

            <Filters />
            <Gallery />

            <div class="text-center mt-12">
                <button class="bg-gradient-to-r from-violet-600 to-indigo-600 hover:from-violet-500 hover:to-indigo-500 text-white px-8 py-3 rounded-xl font-semibold transition-all hover:scale-105 shadow-lg inline-flex items-center gap-2">
                    Browse Full Catalog
                    <ChevronRight class="w-5 h-5" />
                </button>
                <p class="text-sm text-slate-500 mt-4">
                    3,000+ styles available with membership
                </p>
            </div>
        </div>
      </div>
</template>

<script setup lang="ts">
    import { Palette, ChevronRight } from '@lucide/vue';
    import Filters from '../ui/stylecatalog/Filters.vue';
    import Gallery from '../ui/stylecatalog/Gallery.vue';
</script>