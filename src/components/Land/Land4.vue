<script setup>

</script>

<template>
    <div class="absolute z-[10] w-calc([100vw-40rem]) flex justify-start animate-move-right">
        <div class="relative flex flex-col items-center">
            <div class="w-20 h-6 bg-green-500 rounded-full"></div>
        </div>
    </div>
</template>

<style scoped>
@keyframes moveRight {
    0% {
        transform: translateX(-200px);
    }

    100% {
        transform: translateX(150px);
    }
}

.animate-move-right {
    animation: moveRight 5s infinite;
    animation-timing-function: linear;
}
</style>