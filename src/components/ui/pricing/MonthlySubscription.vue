<template>
    <div class="relative bg-white rounded-3xl p-8 shadow-2xl border-4 border-transparent hover:border-violet-400 transition-all hover:scale-105">
        <div class="absolute -top-4 left-1/2 -translate-x-1/2">
            <span class="bg-gradient-to-r from-violet-600 to-indigo-600 text-white px-6 py-2 rounded-full text-sm font-bold shadow-lg">
                MOST POPULAR
            </span>
        </div>
        <div class="text-center mb-8 mt-4">
            <h3 class="text-2xl font-bold text-slate-900 mb-2">Monthly Membership</h3>
            <p class="text-slate-600 mb-6">For serious content creators</p>
            <div class="mb-4">
                <span class="text-6xl font-bold text-slate-900">$39</span>
                <span class="text-slate-600 text-lg">/month</span>
            </div>
            <div class="inline-flex items-center gap-2 bg-violet-100 text-violet-700 px-4 py-2 rounded-full text-sm font-semibold">
                <Star class="w-4 h-4" />
                $49 credits monthly + 10% off extras
            </div>
        </div>
        <ul class="space-y-4 mb-8">
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">$49 in credits every month</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">10% discount on extra credits</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">Unlimited template downloads</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">Priority support access</span>
            </li>
            <li class="flex items-start gap-3">
                <Check class="w-5 h-5 text-green-600 mt-0.5 flex-shrink-0" />
                <span class="text-slate-700">Cancel anytime, no commitment</span>
            </li>
        </ul>
        <a href="https://promptedit.com/" target="_blank" class="w-full block text-center bg-slate-900 hover:bg-slate-800 text-white py-4 rounded-xl font-bold text-lg transition-all hover:scale-105 shadow-lg">
            Start Membership
        </a>
    </div>
</template>

<script lang="ts" setup>
    import { Check, Star } from '@lucide/vue';
</script>