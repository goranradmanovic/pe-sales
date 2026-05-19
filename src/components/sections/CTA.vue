<template>
    <div class="bg-white py-24">
        <div class="container mx-auto px-4">
          <div class="bg-gradient-to-br from-violet-600 via-purple-600 to-indigo-600 rounded-3xl p-12 md:p-16 text-center shadow-2xl relative overflow-hidden">
            <div class="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNjAiIGhlaWdodD0iNjAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGRlZnM+PHBhdHRlcm4gaWQ9ImdyaWQiIHdpZHRoPSI2MCIgaGVpZ2h0PSI2MCIgcGF0dGVyblVuaXRzPSJ1c2VyU3BhY2VPblVzZSI+PHBhdGggZD0iTSAxMCAwIEwgMCAwIDAgMTAiIGZpbGw9Im5vbmUiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS1vcGFjaXR5PSIwLjEiIHN0cm9rZS13aWR0aD0iMSIvPjwvcGF0dGVybj48L2RlZnM+PHJlY3Qgd2lkdGg9IjEwMCUiIGhlaWdodD0iMTAwJSIgZmlsbD0idXJsKCNncmlkKSIvPjwvc3ZnPg==')] opacity-40"></div>
            <div class="relative z-10">
              <Sparkles class="w-16 h-16 text-white mx-auto mb-6 opacity-90" />
              <h2 class="text-4xl md:text-6xl font-bold text-white mb-6">Ready to Create Amazing Content?</h2>
              <p class="text-xl text-white/90 mb-10 max-w-2xl mx-auto leading-relaxed">
                Join thousands of content creators using AI to produce professional-quality content faster than ever before
              </p>
              <div class="flex flex-wrap gap-4 justify-center">
                <a href="#pricing" class="bg-white text-violet-600 px-10 py-4 rounded-xl font-bold text-lg hover:bg-slate-100 transition-all hover:scale-105 shadow-xl flex items-center gap-2">
                  Start Creating Now
                  <ChevronRight class="w-5 h-5" />
                </a>
                <button @click="openTutorial" class="bg-white/10 backdrop-blur-sm border-2 border-white/30 hover:bg-white/20 text-white px-10 py-4 rounded-xl font-bold text-lg transition-all">
                  View Tutorials
                </button>
              </div>
              <div class="mt-8 flex items-center justify-center gap-6 text-white/90 text-sm">
                <div class="flex items-center gap-2">
                  <Check class="w-5 h-5" />
                  <span>No credit card to start</span>
                </div>
                <div class="flex items-center gap-2">
                  <Check class="w-5 h-5" />
                  <span>Cancel anytime</span>
                </div>
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