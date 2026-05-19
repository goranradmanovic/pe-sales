<template>
    <div class="flex gap-4">
        <a href="#" class="w-10 h-10 bg-white/10 hover:bg-white/20 rounded-lg flex items-center justify-center transition-colors">
            <img :src="FacebookIcon" alt="FB" class="w-5 h-5 fill-current text-white" />
        </a>
        <a href="#" class="w-10 h-10 bg-white/10 hover:bg-white/20 rounded-lg flex items-center justify-center transition-colors">
           <img :src="XIcon" alt="X" class="w-5 h-5 fill-current text-white" />
        </a>
        <a href="#" class="w-10 h-10 bg-white/10 hover:bg-white/20 rounded-lg flex items-center justify-center transition-colors">
            <img :src="YoutubeIcon" alt="YT" class="w-5 h-5 fill-current text-white" />
        </a>
    </div>
</template>

<script setup>
    import FacebookIcon from '@/assets/icons/socials/facebook.svg';
    import XIcon from '@/assets/icons/socials/x.svg';
    import YoutubeIcon from '@/assets/icons/socials/youtube.svg';
</script>