<template>
  <div class="bg-gradient-to-br from-slate-50 to-slate-100 py-24">
    <div class="container mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold text-slate-900 mb-4">Frequently Asked Questions</h2>
        <p class="text-lg text-slate-600">Everything you need to know</p>
      </div>

      <div class="max-w-3xl mx-auto space-y-4">
        <div 
          v-for="(card, i) in cards" 
          :key="i" 
          class="bg-white rounded-xl p-6 shadow-md border border-slate-200 hover:shadow-lg transition-all"
        >
          <button 
            @click="toggleCard(i)" 
            class="w-full flex items-center justify-between text-left focus:outline-none group"
            :aria-expanded="activeIndex === i"
          >
            <h3 class="font-bold text-slate-900 text-lg pr-4 group-hover:text-violet-600 transition-colors">
              {{ card.q }}
            </h3>

            <svg 
              class="w-5 h-5 text-slate-400 transition-transform duration-300 flex-shrink-0"
              :class="{ 'rotate-180 text-violet-600': activeIndex === i }"
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>

          <div 
            v-show="activeIndex === i"
            class="mt-3 pt-3 border-t border-slate-100 transition-all duration-300"
          >
            <p class="text-slate-600 leading-relaxed">{{ card.a }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import FQA from '@/types/fqa';

    const cards = ref<FQA[]>([
        { q: "Is this compatible with my editing software?", a: "Yes! PromptEdit works with all major editing software including Premiere Pro, Final Cut Pro, DaVinci Resolve, After Effects, and more." },
        { q: "Can I use this content commercially?", a: "Absolutely! All content created with PromptEdit includes a commercial license, perfect for client work and monetized content." },
        { q: "What happens if I cancel my subscription?", a: "You can cancel anytime with no penalties. Your credits remain valid and you'll keep access until the end of your billing period." },
        { q: "Can I share my account?", a: "No, each account is for individual use only. This ensures fair pricing and optimal performance for all users." },
    ]);

    // Track which index is currently expanded (null means all collapsed)
    const activeIndex = ref<number | null>(null);

    const toggleCard = (index: number) => {
        // If the clicked card is already open, close it. Otherwise, open it.
        activeIndex.value = activeIndex.value === index ? null : index;
    };
</script>