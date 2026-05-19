<template>
    <div class="max-w-6xl mx-auto mb-8">
        <div class="bg-white/10 backdrop-blur-md border border-white/20 rounded-2xl p-6">
            <div class="flex flex-wrap items-center justify-between gap-4">
                <div class="flex flex-wrap items-center gap-4">
                    <button class="flex items-center gap-2 bg-violet-600 hover:bg-violet-500 text-white px-4 py-2 rounded-lg font-semibold transition-all">
                        <Grid3x3 class="w-4 h-4" />
                        My Projects
                    </button>
                    <button class="flex items-center gap-2 bg-white/10 hover:bg-white/20 text-white px-4 py-2 rounded-lg font-semibold transition-all">
                        <Palette class="w-4 h-4" />
                        Style Catalog
                    </button>
                    <button class="flex items-center gap-2 bg-white/10 hover:bg-white/20 text-white px-4 py-2 rounded-lg font-semibold transition-all">
                        <Sliders class="w-4 h-4" />
                        Filters
                    </button>
                </div>
                <div class="flex items-center gap-3 text-white/70 text-sm">
                    <span>Aspect Ratio:</span>
                    <button
                        v-for="(ratio, i) in ratios"
                        :key="i"
                        class="px-3 py-1 bg-white/10 hover:bg-white/20 rounded-lg transition-all"
                    >
                        {{ ratio }}
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
  import { ref } from 'vue';
  import { Palette, Sliders, Grid3x3 } from '@lucide/vue';

  const ratios = ref<string[]>(["16:9", "1:1", "9:16"]);
</script>