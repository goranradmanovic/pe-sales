<template>
  <main class="min-h-screen bg-white">
    <DialogApp v-model="isOpen" />

    <HeaderApp />

    <!-- Sections -->
    <Hero  @open-dialog="openDialog" />
    <AITools />
    <Pricing />
    <TemplatesLibrary />
    <KeyFeatures />
    <Testimonials />
    <FAQ />
    <CTA @open-dialog="openDialog" />
    
    <FooterApp />
  </main>
</template>

<script setup lang="ts">
  import { ref } from 'vue';
  import HeaderApp from './components/base/HeaderApp.vue';
  import DialogApp from './components/ui/common/DialogApp.vue';
  import Hero from './components/sections/Hero.vue';
  import AITools from './components/sections/AITools.vue';
  import Pricing from './components/sections/Pricing.vue';
  import TemplatesLibrary from './components/sections/TemplatesLibrary.vue';
  import KeyFeatures from './components/sections/KeyFeatures.vue';
  import Testimonials from './components/sections/Testimonials.vue';
  import FAQ from './components/sections/FAQ.vue';
  import CTA from './components/sections/CTA.vue';
  import FooterApp from './components/base/FooterApp.vue';

  const isOpen = ref<boolean>(false);
  const openDialog = () => {
    isOpen.value = true;
  };
</script>