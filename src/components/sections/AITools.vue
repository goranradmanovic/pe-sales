
<template>
    <div class="py-24 bg-white">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16">
                <h2 class="text-4xl md:text-5xl font-bold text-slate-900 mb-4">Powerful AI Tools at Your Fingertips</h2>
                <p class="text-lg text-slate-600 max-w-2xl mx-auto">Everything you need to create professional content, all powered by cutting-edge AI</p>
            </div>

          <div class="grid md:grid-cols-2 gap-6 max-w-6xl mx-auto">
            <ImageTools />
            <VideoTools />
            <AudioTools />
            <EditingPlugins />
          </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    import ImageTools from '../ui/aitools/ImageTools.vue';
    import VideoTools from '../ui/aitools/VideoTools.vue';
    import AudioTools from '../ui/aitools/AudioTools.vue';
    import EditingPlugins from '../ui/aitools/EditingPlugins.vue';
</script>