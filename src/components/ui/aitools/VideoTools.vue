<template>
    <div class="group bg-gradient-to-br from-blue-50 to-cyan-50 border-2 border-blue-200 rounded-2xl p-8 hover:shadow-2xl hover:shadow-blue-500/20 transition-all hover:-translate-y-1">
        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-blue-500 to-cyan-600 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
            <Video class="w-8 h-8 text-white" />
        </div>
        <h3 class="text-2xl font-bold text-slate-900 mb-3">Video Tools</h3>
        <p class="text-slate-600 mb-4">Produce cinematic videos with professional-grade AI effects</p>
        <ul class="space-y-2 text-slate-700">
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-blue-600" />
                <span>Clone videos & replicate styles</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-blue-600" />
                <span>Visual effects & enhancements</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-blue-600" />
                <span>Cinematic films & commercials</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-blue-600" />
                <span>Reels & YouTube content</span>
            </li>
        </ul>
    </div>
</template>

<script lang="ts" setup>
    import { Check, Video } from '@lucide/vue';
</script>