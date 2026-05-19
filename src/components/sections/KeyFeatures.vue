<template>
    <div class="bg-gradient-to-br from-violet-50 via-white to-indigo-50 py-24">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold text-slate-900 mb-4">Why Content Creators Choose Us</h2>
            <p class="text-lg text-slate-600">Everything you need, backed by our guarantee</p>
          </div>

          <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
              <div v-for="(feature, i) in features" :key="i" class="bg-white rounded-2xl p-6 shadow-lg border border-slate-200 hover:shadow-xl transition-all hover:-translate-y-1">
                <div :class="`w-14 h-14 rounded-xl bg-gradient-to-br ${feature?.color} flex items-center justify-center mb-4`">
                  <component :is="feature?.icon" class="w-7 h-7 text-white" />
                </div>
                <h3 class="text-xl font-bold text-slate-900 mb-2">{{ feature?.title }}</h3>
                <p class="text-slate-600 leading-relaxed">{{ feature?.desc }}</p>
              </div>
          </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
    import { ref } from 'vue';
    import { Check, Download, Zap, Shield, Star, Layers } from '@lucide/vue';
    import Feature from '@/types/feature';

    const features = ref<Feature[]>([
        { icon: Zap, title: "Pay As You Go", desc: "No forced subscriptions. Buy credits when you need them, use them when you want.", color: "from-yellow-500 to-amber-600" },
        { icon: Shield, title: "100% Money Back", desc: "Not satisfied? Get a full refund within 30 days on unused credits. No questions asked.", color: "from-green-500 to-emerald-600" },
        { icon: Check, title: "Commercial License", desc: "Use all generated content commercially. Perfect for client work and monetized content.", color: "from-blue-500 to-cyan-600" },
        { icon: Download, title: "Unlimited Downloads", desc: "Active members get unlimited access to our entire templates and assets library.", color: "from-purple-500 to-violet-600" },
        { icon: Layers, title: "All Editing Software", desc: "Compatible with Premiere, Final Cut, DaVinci, After Effects, and more.", color: "from-pink-500 to-rose-600" },
        { icon: Star, title: "No Account Sharing", desc: "One account per user ensures fair pricing and optimal performance for everyone.", color: "from-indigo-500 to-purple-600" },
    ]);
</script>