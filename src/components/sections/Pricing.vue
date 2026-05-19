<template>
    <div id="pricing" class="bg-gradient-to-br from-slate-900 via-violet-900 to-slate-900 py-24">
        <div class="container mx-auto px-4">
          <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">Simple, Flexible Pricing</h2>
            <p class="text-lg text-white/80 max-w-2xl mx-auto">Choose the plan that works best for you. No hidden fees, cancel anytime</p>
          </div>

          <div class="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
            <OneTimeOffer />
            <MonthlySubscription />
          </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    import MonthlySubscription from '../ui/pricing/MonthlySubscription.vue';
    import OneTimeOffer from '../ui/pricing/OneTimeOffer.vue';
</script>