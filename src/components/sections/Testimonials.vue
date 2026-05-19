<template>
    <div class="bg-white py-24">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl font-bold text-slate-900 mb-4">Trusted by Thousands of Creators</h2>
            <p class="text-lg text-slate-600">See what our community has to say</p>
          </div>

          <div class="grid md:grid-cols-3 gap-6 max-w-6xl mx-auto">
              <div v-for="(testemonial, i) in testimonials" :key="i" class="bg-gradient-to-br from-slate-50 to-slate-100 border-2 border-slate-200 rounded-2xl p-6 hover:border-violet-400 hover:shadow-xl transition-all">
                <div class="flex gap-1 mb-4">
                    <Star v-for="(item, j) in ratingsArr(testemonial?.rating)" :key="j" class="w-5 h-5 fill-amber-400 text-amber-400" />
                </div>
                <p class="text-slate-700 mb-6 leading-relaxed">"{{ testemonial?.text }}"</p>
                <div class="flex items-center gap-3">
                  <div class="w-12 h-12 rounded-full bg-gradient-to-br from-violet-500 to-indigo-600 flex items-center justify-center text-white font-bold text-lg">
                    {{ testemonial.name.split(' ').map((n: string[]) => n[0]).join('') }}
                  </div>
                  <div>
                    <div class="font-semibold text-slate-900">{{ testemonial?.name }}</div>
                    <div class="text-sm text-slate-600">{{ testemonial?.role }}</div>
                  </div>
                </div>
              </div>
          </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import { Star } from '@lucide/vue';
    import Testemonial from '@/types/testemonial';

    const testimonials = ref<Testemonial[]>([
        { name: "Sarah Martinez", role: "YouTube Creator", rating: 5, text: "PromptEdit has completely transformed my workflow. I save hours every week and the quality is incredible!" },
        { name: "James Chen", role: "Video Editor", rating: 4, text: "The pay-as-you-go model is perfect for freelancers like me. No more wasting money on subscriptions I don't fully use." },
        { name: "Emily Rodriguez", role: "Social Media Manager", rating: 5, text: "The template library alone is worth the membership. My content has never looked better!" },
    ]);

    const ratingsArr = (rating: number) => Array.from({ length: rating });
</script>