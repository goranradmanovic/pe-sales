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

<script setup>
  import { Sparkles, ChevronRight, Check } from '@lucide/vue';

  const emit = defineEmits(['openDialog']);

  const openTutorial = () => {
    emit('openDialog');
  };
</script>