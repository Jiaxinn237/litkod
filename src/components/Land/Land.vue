<script setup>

</script>

<template>
    <div class="absolute z-[10] w-calc([100vw-40rem]) flex justify-start animate-move-right">
        <div class="relative flex flex-col items-center">
            <div class="w-24 h-8 bg-green-500 rounded-full"></div>
            <div class="absolute top-6 w-6 h-8 bg-green-500 rounded-full z-[1]"></div>
            <div class="w-16 h-6 bg-green-500 rounded-full mt-2"></div>
        </div>
    </div>
</template>

<style scoped>
@keyframes moveRight {
    0% {
        transform: translateX(-300px);
    }

    100% {
        transform: translateX(300px);
    }
}

.animate-move-right {
    animation: moveRight 5s infinite;
    animation-timing-function: linear;
}
</style>