<template>
    <div class="relative bg-white rounded-3xl p-8 shadow-2xl border-4 border-transparent hover:border-violet-400 transition-all hover:scale-105">
        <div class="absolute -top-4 left-1/2 -translate-x-1/2">
            <span class="bg-gradient-to-r from-amber-500 to-orange-600 text-white px-6 py-2 rounded-full text-sm font-bold shadow-lg">
                BEST VALUE
            </span>
        </div>

        <div class="text-center mb-8 mt-4">
            <h3 class="text-2xl font-bold text-slate-900 mb-2">One-Time Credits</h3>
            <p class="text-slate-600 mb-6">Perfect for trying out the platform</p>
            <div class="mb-4">
                <span class="text-6xl font-bold text-slate-900">$98</span>
            </div>
            <div class="inline-flex items-center gap-2 bg-green-100 text-green-700 px-4 py-2 rounded-full text-sm font-semibold">
                <Zap class="w-4 h-4" />
                Get $110 in credits • Save 10%
            </div>
        </div>
        <ul class="space-y-4 mb-8">
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">$110 worth of AI credits</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">Access all AI tools</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">Credits never expire</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">Commercial license included</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">30-day money back guarantee</span>
            </li>
        </ul>
        <a href="https://www.contentcreator.com/prompt-edit" target="_blank" class="w-full block text-center bg-gradient-to-r from-violet-600 to-indigo-600 hover:from-violet-500 hover:to-indigo-500 text-white py-4 rounded-xl font-bold text-lg transition-all hover:scale-105 shadow-lg">
            Get Started Now
        </a>
    </div>
</template>

<script lang="ts" setup>
    import { Check, Zap } from '@lucide/vue';
</script>