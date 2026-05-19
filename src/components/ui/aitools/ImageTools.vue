<template>
    <div class="group bg-gradient-to-br from-pink-50 to-rose-50 border-2 border-pink-200 rounded-2xl p-8 hover:shadow-2xl hover:shadow-pink-500/20 transition-all hover:-translate-y-1">
        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-pink-500 to-rose-600 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
            <Image class="w-8 h-8 text-white" />
        </div>
        <h3 class="text-2xl font-bold text-slate-900 mb-3">Image Tools</h3>
        <p class="text-slate-600 mb-4">Create stunning visuals with AI-powered image generation and editing</p>
        <ul class="space-y-2 text-slate-700">
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-pink-600" />
                <span>Image clones & variations</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-pink-600" />
                <span>Social media posts & graphics</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-pink-600" />
                <span>Thumbnail & ad creation</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-pink-600" />
                <span>Professional editing tools</span>
            </li>
        </ul>
    </div>
</template>

<script lang="ts" setup>
    import { Check, Image } from '@lucide/vue';
</script>