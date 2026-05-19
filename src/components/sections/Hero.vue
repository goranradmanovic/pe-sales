<template>
    <div class="relative overflow-hidden bg-gradient-to-br from-violet-50 via-white to-indigo-50">
        <div class="container mx-auto px-4 py-24 relative z-10">
          <div class="text-center max-w-5xl mx-auto">
            <div class="inline-flex items-center gap-2 bg-violet-100 border border-violet-200 rounded-full px-5 py-2 mb-8">
              <Sparkles class="w-4 h-4 text-violet-600" />
              <span class="text-sm font-semibold text-violet-700">The AI Tools Marketplace</span>
            </div>

            <h1 class="text-5xl md:text-7xl font-bold text-slate-900 mb-6 leading-tight">
              Your AI Creative Studio,
              <span class="block bg-gradient-to-r from-violet-600 via-indigo-600 to-purple-600 bg-clip-text text-transparent mt-2">
                All in One Place
              </span>
            </h1>

            <p class="text-xl text-slate-600 mb-10 max-w-3xl mx-auto leading-relaxed">
              Stop juggling multiple subscriptions. Access cutting-edge AI tools for images, videos, and audio with our simple pay-as-you-go credit system. It's like a grocery store for AI.
            </p>

            <div class="flex flex-wrap gap-4 justify-center mb-12">
              <a href="#pricing" class="bg-gradient-to-r from-violet-600 to-indigo-600 hover:from-violet-500 hover:to-indigo-500 text-white px-10 py-4 rounded-xl font-semibold flex items-center gap-2 shadow-xl shadow-violet-500/30 transition-all hover:scale-105">
                Start Creating Now
                <ChevronRight class="w-5 h-5" />
              </a>
              <button @click="openTutorial" class="bg-white border-2 border-slate-300 hover:border-violet-400 hover:bg-violet-50 text-slate-700 px-10 py-4 rounded-xl font-semibold transition-all">
                Watch Tutorial
              </button>
            </div>

            <div class="max-w-3xl mx-auto mb-8">
              <div class="relative group">
                <div class="absolute inset-0 bg-gradient-to-r from-violet-600 to-indigo-600 rounded-2xl blur-xl opacity-20 group-hover:opacity-30 transition-opacity"></div>
                <div class="relative bg-white rounded-2xl shadow-2xl border-2 border-violet-200 overflow-hidden">
                  <div class="flex items-center p-2 flex-wrap">
                    <div class="flex items-center gap-3 flex-1 px-4">
                      <Search class="w-5 h-5 text-violet-600" />
                      <input
                        v-model="aiSearch"
                        type="text"
                        placeholder="What would you like to create? Try 'cinematic landscape' or 'energetic voiceover'..."
                        class="flex-1 py-3 text-slate-700 placeholder:text-slate-400 focus:outline-none"
                      />
                    </div>
                    <button class="bg-gradient-to-r from-violet-600 to-indigo-600 hover:from-violet-500 hover:to-indigo-500 text-white px-6 py-3 rounded-xl font-semibold transition-all hover:scale-105 flex items-center mx-auto gap-2">
                      Generate
                      <Sparkles class="w-4 h-4" />
                    </button>
                  </div>
                  <div class="px-6 pb-4 flex flex-wrap gap-2 mt-2">
                    <span class="text-xs text-slate-500">
                      Try:
                    </span>
                      <button
                        v-for="(tag, i) in tags"
                        :key="i"
                        class="text-xs bg-violet-50 hover:bg-violet-100 text-violet-700 px-3 py-1 rounded-full transition-colors font-medium"
                      >
                        {{ tag }}
                      </button>
                  </div>
                </div>
              </div>
            </div>

            <!-- Trust Badges -->
            <div class="flex flex-wrap items-center justify-center gap-8 text-sm text-slate-600">
              <div class="flex items-center gap-2">
                <Check class="w-5 h-5 text-green-600" />
                <span>No subscription required</span>
              </div>
              <div class="flex items-center gap-2">
                <Check class="w-5 h-5 text-green-600" />
                <span>Commercial license included</span>
              </div>
              <div class="flex items-center gap-2">
                <Check class="w-5 h-5 text-green-600" />
                <span>30-day money back</span>
              </div>
            </div>
          </div>
        </div>
    </div>
</template>

<script setup lang="ts">
  import { ref } from 'vue';
  import { Sparkles, ChevronRight, Check, Search } from '@lucide/vue';

  const emit = defineEmits(['openDialog']);

  const tags = ref<string[]>([
    "Thumbnail Design",
    "Product Video",
    "Podcast Intro",
    "Social Post",
  ]);

  const aiSearch = ref<string>('');

  const openTutorial = () => {
    emit('openDialog');
  };
</script>