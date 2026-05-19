<template>
    <dialog 
        ref="dialogRef"
        @cancel="handleNativeCancel"
        class="fixed inset-0 m-auto w-full max-w-xl rounded-2xl bg-white p-6 text-left shadow-xl border border-slate-100 backdrop:bg-slate-900/40 backdrop:backdrop-blur-sm open:animate-in open:fade-in open:zoom-in-95 open:duration-200 focus:outline-none"
    >
        <div class="flex items-center justify-between mb-4">
            <h3 class="text-xl font-bold text-slate-900">
                Watch Our Quick Tutorial
            </h3>
            <button 
                @click="isOpen = false"
                class="rounded-lg p-1.5 text-slate-400 hover:text-slate-600 hover:bg-slate-100 transition-colors focus:outline-none"
                aria-label="Close dialog"
            >
                <svg class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
                </svg>
            </button>
        </div>

        <div class="w-full aspect-video rounded-lg overflow-hidden bg-slate-900">
            <iframe
            src="https://fast.wistia.net/embed/iframe/eu37od3pav?web_component=true&amp;seo=true"
            title="Ai tool vs marketplace Video"
            allow="autoplay; fullscreen"
            allowtransparency="true"
            frameborder="0"
            scrolling="no"
            class="w-full h-full"
            name="wistia_embed"
            ></iframe>
        </div>

        <!-- Footer Actions Area -->
        <div class="mt-6 flex justify-end gap-3">
            <button 
                @click="isOpen = false"
                class="px-4 py-2 text-sm font-medium text-slate-600 hover:text-slate-900 bg-slate-50 hover:bg-slate-100 rounded-lg transition-colors"
            >
                Cancel
            </button>
        </div>
    </dialog>
</template>

<script lang="ts" setup>
    import { ref, watch, nextTick } from 'vue';

    const isOpen = defineModel<boolean>({ required: true });
    const dialogRef = ref<HTMLDialogElement | null>(null);

    // Watch the model state to call native DOM methods
    watch(isOpen, async (shouldOpen) => {
        // Wait for the component to completely mount so dialogRef is populated
        await nextTick();

        if (!dialogRef.value) return;

        if (shouldOpen) {
            if (!dialogRef.value.open) {
            dialogRef.value.showModal();
            }
        } else {
            if (dialogRef.value.open) {
            dialogRef.value.close();
            }
        }
    }, { immediate: true });

    const handleNativeCancel = (event: Event) => {
        event.preventDefault(); 
        isOpen.value = false; 
    };
</script>