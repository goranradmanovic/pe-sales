<template>
    <div class="max-w-6xl mx-auto grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
            v-for="(item, i) in projects"
            :key="i"
            class="group relative bg-white/5 backdrop-blur-sm border border-white/10 rounded-2xl overflow-hidden hover:border-violet-400 transition-all hover:scale-105 cursor-pointer"
        >
            <div :class="`aspect-video bg-gradient-to-br ${item.gradient} relative overflow-hidden`">
                <img :src="item.image" :alt="item.title" class="absolute inset-0 w-full h-full object-cover" />
                
                <div class="absolute inset-0 bg-black/20 group-hover:bg-black/10 transition-all"></div>
                <div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity">
                    <div class="bg-white/20 backdrop-blur-sm rounded-full p-4">
                        <Play class="w-8 h-8 text-white" />
                    </div>
                </div>
                <div class="absolute top-3 left-3">
                    <span class="bg-black/50 backdrop-blur-sm text-white text-xs px-3 py-1 rounded-full font-semibold">
                        {{ item?.type }}
                    </span>
                </div>
            </div>

            <div class="p-4">
                <h3 class="font-bold text-white mb-1">
                    {{ item?.title }}
                </h3>
                <div class="flex items-center justify-between">
                    <span class="text-sm text-white/60">
                        {{ item?.style }} Style
                    </span>
                    <button class="text-cyan-400 hover:text-cyan-300 text-sm font-semibold transition-colors">
                        Edit
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    import { ref } from 'vue';
    import GalleryArtItem from '@/types/gallery';
    import { Play } from '@lucide/vue';

    const projects = ref<GalleryArtItem[]>([
        {
            type: "Image",
            title: "Cinematic Sunset",
            style: "Landscape",
            gradient: "from-orange-500 to-pink-600",
            image: "https://images.unsplash.com/photo-1495567720989-cebdbdd97913?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        },
        {
            type: "Video",
            title: "Product Demo",
            style: "Commercial",
            gradient: "from-blue-500 to-cyan-600",
            image: "https://images.unsplash.com/photo-1571406396589-600f094f4254?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        },
        {
            type: "Audio",
            title: "Voiceover Track",
            style: "Professional",
            gradient: "from-purple-500 to-violet-600",
            image: "https://images.unsplash.com/photo-1659083725992-9d88c12e719c?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        },
        {
            type: "Image",
            title: "Social Media Post",
            style: "Modern",
            gradient: "from-green-500 to-emerald-600",
            image: "https://images.unsplash.com/photo-1643503640904-75c1a2093570?q=80&w=1170&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        },
        {
            type: "Video",
            title: "YouTube Intro",
            style: "Dynamic",
            gradient: "from-red-500 to-rose-600",
            image: "https://images.unsplash.com/photo-1611162616475-46b635cb6868?q=80&w=1074&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        },
        {
            type: "Image",
            title: "Thumbnail Design",
            style: "Bold",
            gradient: "from-amber-500 to-orange-600",
            image: "https://images.unsplash.com/photo-1626785774625-ddcddc3445e9?q=80&w=1171&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
        },
    ]);
</script>