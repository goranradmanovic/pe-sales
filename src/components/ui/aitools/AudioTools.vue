<template>
    <div class="group bg-gradient-to-br from-purple-50 to-violet-50 border-2 border-purple-200 rounded-2xl p-8 hover:shadow-2xl hover:shadow-purple-500/20 transition-all hover:-translate-y-1">
        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-purple-500 to-violet-600 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
            <Mic class="w-8 h-8 text-white" />
        </div>
        <h3 class="text-2xl font-bold text-slate-900 mb-3">Audio Tools</h3>
        <p class="text-slate-600 mb-4">Generate professional audio content with AI voice technology</p>
        <ul class="space-y-2 text-slate-700">
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-purple-600" />
                <span>Professional voiceovers</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-purple-600" />
                <span>Voice cloning & swapping</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-purple-600" />
                <span>Sound effects library</span>
            </li>
            <li class="flex items-center gap-2">
                <Check class="w-4 h-4 text-purple-600" />
                <span>Music generation</span>
            </li>
        </ul>
    </div>
</template>

<script lang="ts" setup>
    import { Check, Mic } from '@lucide/vue';
</script>