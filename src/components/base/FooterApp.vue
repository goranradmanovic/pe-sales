<template>
    <div class="bg-slate-900 text-white py-16">
        <div class="container mx-auto px-4">
            <div class="grid md:grid-cols-5 gap-8 mb-12">
                <div class="md:col-span-2">
                    <div class="flex items-center gap-2 mb-4">
                        <Logo />
                        <span class="text-2xl font-bold">PromptEdit</span>
                    </div>
                    <p class="text-white/70 mb-6 max-w-sm leading-relaxed">
                        Your all-in-one AI creative studio. Access powerful tools for images, videos, and audio with flexible pay-as-you-go pricing.
                    </p>
                    <SocialLinks />
                </div>

                <div>
                    <h3 class="font-bold text-lg mb-4">Product</h3>
                    <ProductLinks />
                </div>

                <div>
                    <h3 class="font-bold text-lg mb-4">Support</h3>
                    <SupportLinks />
                </div>

                <div>
                    <h3 class="font-bold text-lg mb-4">Legal</h3>
                    <LegalLinks />
                </div>
            </div>

            <div class="border-t border-white/10 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center gap-4 text-white/60 text-sm">
                    <p>&copy; 2026 PromptEdit. All rights reserved.</p>
                    <p class="flex items-center gap-2">
                        <Shield class="w-4 h-4" />
                        100% Secure Payment • 30-Day Money Back Guarantee
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    import { Shield } from '@lucide/vue';
    import Logo from './Logo.vue';
    import SocialLinks from '../ui/footer/SocialLinks.vue';
    import ProductLinks from '../ui/footer/ProductLinks.vue';
    import SupportLinks from '../ui/footer/SupportLinks.vue';
    import LegalLinks from '../ui/footer/LegalLinks.vue';
</script>