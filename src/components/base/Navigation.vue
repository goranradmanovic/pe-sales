<template>
  <nav class="border-b border-slate-200 bg-white/80 backdrop-blur-md sticky top-0 z-50">
    <div class="container mx-auto px-4 py-4">
      <div class="flex items-center justify-between">
        <!-- Logo Area -->
        <div class="flex items-center gap-2">
          <Logo />
          <span class="text-2xl font-bold bg-gradient-to-r from-violet-600 to-indigo-600 bg-clip-text text-transparent">PromptEdit</span>
        </div>

        <!-- Desktop Navigation Links (Hidden on small screens, flex on md and up) -->
        <div class="hidden md:flex items-center gap-6">
          <NavItems />
        </div>

        <!-- Mobile Hamburger Button (Visible on small screens, hidden on md and up) -->
        <div class="md:hidden flex items-center">
          <button @click="isMenuOpen = !isMenuOpen" class="text-slate-600 hover:text-slate-900 focus:outline-none" aria-label="Toggle menu">
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Dropdown Menu (Conditionally rendered/shown) -->
      <div v-show="isMenuOpen" class="md:hidden mt-4 pt-4 border-t border-slate-100 flex flex-col gap-4">
        <NavItems />
      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
  import { ref } from 'vue';
  import NavItems from './NavItems.vue';
  import Logo from './Logo.vue';

  const isMenuOpen = ref<boolean>(false);
</script>