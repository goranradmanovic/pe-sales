<template>
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 max-w-7xl mx-auto">
        <div
            v-for="(style, i) in styles"
            :key="i"
            class="group relative aspect-square rounded-2xl overflow-hidden cursor-pointer border-2 border-slate-200 hover:border-violet-400 transition-all hover:scale-105 hover:shadow-2xl"
            :class="`bg-gradient-to-br ${style.color}`"
        >
            <!-- Background Image -->
            <img :src="style.image" alt="style.name" class="absolute inset-0 w-full h-full object-cover" />

            <!-- Overlay -->
            <div class="absolute inset-0 bg-black/20 group-hover:bg-black/40 transition-all"></div>

            <!-- Play Button on Hover -->
            <div class="absolute inset-0 flex items-center justify-center opacity-0 group-hover:opacity-100 transition-opacity">
                <div class="bg-white/20 backdrop-blur-md rounded-full p-4 group-hover:scale-110 transition-transform">
                    <Play class="w-6 h-6 text-white" />
                </div>
            </div>

            <!-- Style Info -->
            <div class="absolute bottom-0 left-0 right-0 p-4 bg-gradient-to-t from-black/80 to-transparent">
                <h3 class="font-bold text-white mb-1">
                    {{ style.name }}
                </h3>
                <p class="text-xs text-white/80">
                    {{ style.mood }} Mood
                </p>
            </div>

            <!-- Quick Apply Badge -->
            <div class="absolute top-3 right-3 opacity-0 group-hover:opacity-100 transition-opacity">
                <button class="bg-violet-600 hover:bg-violet-500 text-white text-xs px-3 py-1.5 rounded-full font-semibold shadow-lg">
                    Apply
                </button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
    import { Play } from '@lucide/vue';
    import { ref } from 'vue';
    import GalleryCatalogItem  from '@/types/gallery';

    const styles = ref<GalleryCatalogItem[]>([
        {
            name: "Cinematic Dream",
            mood: "Dramatic",
            color: "from-orange-400 via-red-500 to-purple-600",
            image: "https://images.unsplash.com/photo-1501619757722-90657a99803b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxjaW5lbWF0aWMlMjBkcmFtYXRpYyUyMHN1bnNldCUyMGxhbmRzY2FwZXxlbnwxfHx8fDE3NzkxODg3NDh8MA&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Ocean Breeze",
            mood: "Calm",
            color: "from-cyan-400 via-blue-500 to-indigo-600",
            image: "https://images.unsplash.com/photo-1468581264429-2548ef9eb732?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxjYWxtJTIwb2NlYW4lMjB3YXZlcyUyMHBlYWNlZnVsJTIwYmx1ZSUyMHdhdGVyfGVufDF8fHx8MTc3OTE4ODc0OXww&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Neon Nights",
            mood: "Energetic",
            color: "from-pink-500 via-purple-500 to-indigo-600",
            image: "https://images.unsplash.com/photo-1542902093-d55926049754?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxuZW9uJTIwbGlnaHRzJTIwY2l0eSUyMG5pZ2h0JTIwdmlicmFudHxlbnwxfHx8fDE3NzkxODg3NTB8MA&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Forest Mist",
            mood: "Natural",
            color: "from-green-400 via-emerald-500 to-teal-600",
            image: "https://images.unsplash.com/photo-1448375240586-882707db888b?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxmb3Jlc3QlMjBtaXN0JTIwbmF0dXJlJTIwZ3JlZW4lMjB0cmVlc3xlbnwxfHx8fDE3NzkxODg3NTB8MA&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Golden Hour",
            mood: "Warm",
            color: "from-yellow-400 via-orange-500 to-red-600",
            image: "https://images.unsplash.com/photo-1529117218-5329a8d5e0f5?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxnb2xkZW4lMjBob3VyJTIwd2FybSUyMHN1bnNldCUyMGdsb3d8ZW58MXx8fHwxNzc5MTg4NzUxfDA&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Arctic Frost",
            mood: "Cool",
            color: "from-blue-300 via-cyan-400 to-teal-500",
            image: "https://images.unsplash.com/photo-1545586860-95d2040c1680?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxhcmN0aWMlMjBmcm9zdCUyMGljZSUyMGJsdWUlMjB3aW50ZXJ8ZW58MXx8fHwxNzc5MTg4NzUxfDA&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Sunset Glow",
            mood: "Vibrant",
            color: "from-rose-400 via-orange-500 to-amber-600",
            image: "https://images.unsplash.com/photo-1519977552815-08175cb3375a?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwyfHx2aWJyYW50JTIwc3Vuc2V0JTIwb3JhbmdlJTIwcGluayUyMHNreXxlbnwxfHx8fDE3NzkxODg3NTJ8MA&ixlib=rb-4.1.0&q=80&w=1080",
        },
        {
            name: "Deep Space",
            mood: "Mysterious",
            color: "from-indigo-600 via-purple-700 to-slate-900",
            image: "https://images.unsplash.com/photo-1677926405168-fa86268b7295?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxkZWVwJTIwc3BhY2UlMjBzdGFycyUyMGdhbGF4eSUyMG5lYnVsYXxlbnwxfHx8fDE3NzkxODg3NTJ8MA&ixlib=rb-4.1.0&q=80&w=1080",
        },
    ]);
</script>