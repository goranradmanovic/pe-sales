<template>
    <div class="group bg-gradient-to-br from-amber-50 to-orange-50 border-2 border-amber-200 rounded-2xl p-8 hover:shadow-2xl hover:shadow-amber-500/20 transition-all hover:-translate-y-1">
        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-amber-500 to-orange-600 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
            <Layers class="w-8 h-8 text-white" />
        </div>
        <h3 class="text-2xl font-bold text-slate-900 mb-3">Editing Plugins</h3>
        <p class="text-slate-600 mb-4">Seamlessly integrated tools for your favorite editing software</p>
        <ul class="space-y-2 text-slate-700">
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-amber-600" />
                <span>Browser-free integration</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-amber-600" />
                <span>Direct software plugins</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-amber-600" />
                <span>All major editors supported</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-amber-600" />
                <span>Streamlined workflow</span>
            </li>
        </ul>
    </div>
</template>

<script lang="ts" setup>
    import { Check, Layers } from '@lucide/vue';
</script>