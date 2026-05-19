<template>
  <div class="bg-white py-16 border-b border-slate-100">
    <div class="container mx-auto px-4">
      <!-- Section Header -->
      <div class="max-w-2xl mx-auto text-center mb-12">
        <span class="text-xs font-bold tracking-wider text-violet-600 uppercase bg-violet-50 px-3 py-1 rounded-full">
          Now Available
        </span>
        <h2 class="text-3xl font-bold text-slate-900 mt-3 mb-4">
          Powered by Next-Gen AI Models
        </h2>
        <p class="text-slate-600">
          Get instant, unrestricted access to the industry's leading video, image, and speed-optimized foundation models.
        </p>
      </div>

      <!-- Models Grid Layout -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 max-w-6xl mx-auto">
        <div 
          v-for="model in aiModels" 
          :key="model.name"
          class="group bg-slate-50 rounded-2xl border border-slate-200/60 overflow-hidden hover:border-violet-200 hover:bg-white shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col"
        >
          <!-- Model Image / Cover Container -->
          <div class="relative aspect-video bg-slate-900 overflow-hidden w-full">
            <img 
              :src="model.image" 
              :alt="model.name" 
              class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500 opacity-90 group-hover:opacity-100"
              loading="lazy"
            />
            <!-- Quick tag badge overlay -->
            <div class="absolute top-3 left-3">
              <span class="text-[10px] font-bold tracking-wider text-white uppercase bg-slate-950/60 backdrop-blur-md px-2.5 py-1 rounded-md">
                {{ model.type }}
              </span>
            </div>
          </div>
          
          <!-- Content Details Area -->
          <div class="p-5 flex-grow flex flex-col justify-between">
            <div>
              <h3 class="font-extrabold text-slate-800 group-hover:text-violet-600 text-lg tracking-tight transition-colors mb-1">
                {{ model.name }}
              </h3>
              <p class="text-xs text-slate-500 leading-relaxed">
                {{ model.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
  import { ref } from 'vue';
  import AIModel from '../../types/aimodel';

  const aiModels = ref<AIModel[]>([
    { 
      name: 'VEO 3.1 Fast', 
      type: 'Video / Speed', 
      description: 'Google’s optimized generative video model built for lightning-fast iterations and rough cuts.',
      image: 'https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=600&auto=format&fit=crop' 
    },
    { 
      name: 'Sora 2', 
      type: 'Cinematic', 
      description: 'OpenAI’s photorealistic cinematic physics engine, boasting exceptional multi-character prompt adherence.',
      image: 'https://images.unsplash.com/photo-1579783902614-a3fb3927b6a5?q=80&w=600&auto=format&fit=crop' 
    },
    { 
      name: 'Nano Banana', 
      type: 'Lightweight Image', 
      description: 'Google’s hyper-efficient Gemini image model engineered for rapid, conversational graphics editing.',
      image: 'https://images.unsplash.com/photo-1614741118887-7a4ee193a5fa?q=80&w=600&auto=format&fit=crop' 
    },
    { 
      name: 'Nano Banana Pro', 
      type: 'Advanced Image', 
      description: 'The advanced tier of the Flash image matrix, handling crisp layout text rendering and maps directly inside assets.',
      image: 'https://images.unsplash.com/photo-1634017839464-5c339ebe3cb4?q=80&w=600&auto=format&fit=crop' 
    },
    { 
      name: 'Kling 2.6', 
      type: 'High-Fidelity', 
      description: 'Cinema-grade generation with native simultaneous audio tracking, speech, and sound effect mixing.',
      image: 'https://images.unsplash.com/photo-1620641788421-7a1c342ea42e?q=80&w=600&auto=format&fit=crop' 
    },
    { 
      name: 'Kling 2.5 Turbo', 
      type: 'Generation', 
      description: 'High-volume video creation pipeline model balancing lightning generation speed with strict character consistency.',
      image: 'https://images.unsplash.com/photo-1541701494587-cb58502866ab?q=80&w=600&auto=format&fit=crop' 
    },
  ]);
</script>