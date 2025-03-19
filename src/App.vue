<script setup>
import StarryNight from '../src/components/StarryNight.vue'
import Earth from './components/Earth.vue';
</script>

<template>
    <div class="relative w-full h-screen flex items-center justify-center">
        <StarryNight />

        <div class="inset-0 z-[2]">
            <Earth />
        </div>
    </div>
</template>
