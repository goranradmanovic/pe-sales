<template>
    <div class="bg-white py-24">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <div class="inline-flex items-center gap-2 bg-violet-100 border border-violet-200 rounded-full px-5 py-2 mb-6">
              <Download class="w-4 h-4 text-violet-600" />
              <span class="text-sm font-semibold text-violet-700">Included with Membership</span>
            </div>
            <h2 class="text-4xl md:text-5xl font-bold text-slate-900 mb-4">Complete Creator Templates Library</h2>
            <p class="text-lg text-slate-600 max-w-2xl mx-auto">Over 74,000 professional assets to supercharge your content creation</p>
          </div>

          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-6 max-w-6xl mx-auto mb-12">
              <div v-for="(item, i) in cards" :key="i" :class="`bg-gradient-to-br ${item?.bg} border-2 border-slate-200 rounded-2xl p-6 hover:shadow-xl transition-all hover:-translate-y-1`">
                <div :class="`w-14 h-14 rounded-xl bg-gradient-to-br ${item?.color} flex items-center justify-center mb-4`">
                  <component :is="item?.icon" class="w-7 h-7 text-white" />
                </div>
                <h3 class="text-2xl font-bold text-slate-900 mb-1">{{item?.title }}</h3>
                <p class="text-slate-600">{{ item?.desc }}</p>
              </div>
          </div>

          <div class="bg-gradient-to-br from-slate-50 to-slate-100 rounded-2xl p-8 max-w-4xl mx-auto border border-slate-200">
            <div class="grid md:grid-cols-2 gap-6">
              <div>
                <h3 class="text-xl font-bold text-slate-900 mb-4">What's Included:</h3>
                <ul class="space-y-3 text-slate-700">
                  <li class="flex items-center gap-3">
                    <Check class="w-5 h-5 text-green-600 flex-shrink-0" />
                    <span>Unlimited downloads with membership</span>
                  </li>
                  <li class="flex items-center gap-3">
                    <Check class="w-5 h-5 text-green-600 flex-shrink-0" />
                    <span>Works with all editing software</span>
                  </li>
                  <li class="flex items-center gap-3">
                    <Check class="w-5 h-5 text-green-600 flex-shrink-0" />
                    <span>Regular updates with new assets</span>
                  </li>
                </ul>
              </div>
              <div>
                <h3 class="text-xl font-bold text-slate-900 mb-4">Perfect For:</h3>
                <ul class="space-y-3 text-slate-700">
                  <li class="flex items-center gap-3">
                    <Check class="w-5 h-5 text-violet-600 flex-shrink-0" />
                    <span>YouTube creators</span>
                  </li>
                  <li class="flex items-center gap-3">
                    <Check class="w-5 h-5 text-violet-600 flex-shrink-0" />
                    <span>Social media influencers</span>
                  </li>
                  <li class="flex items-center gap-3">
                    <Check class="w-5 h-5 text-violet-600 flex-shrink-0" />
                    <span>Professional video editors</span>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import { Check, Download, Palette, Music, Film, Layers } from '@lucide/vue';
    import Template from '@/types/template';

    const cards = ref<Template[]>([
        { icon: Palette, title: "4,000+ LUTs", desc: "Color grading presets", color: "from-pink-500 to-rose-600", bg: "from-pink-50 to-rose-50" },
        { icon: Music, title: "60,000+ Sounds", desc: "Professional sound effects", color: "from-blue-500 to-cyan-600", bg: "from-blue-50 to-cyan-50" },
        { icon: Film, title: "3,000+ Animations", desc: "Text animation presets", color: "from-purple-500 to-violet-600", bg: "from-purple-50 to-violet-50" },
        { icon: Layers, title: "7,000+ Assets", desc: "Overlays & backgrounds", color: "from-amber-500 to-orange-600", bg: "from-amber-50 to-orange-50" },
    ]);
</script>