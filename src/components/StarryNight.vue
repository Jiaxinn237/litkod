<script setup>
import { onMounted } from "vue";

onMounted(() => {
    const canvas = document.getElementById("starryCanvas");
    const ctx = canvas.getContext("2d");

    // Set canvas size
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;

    // Generate random stars
    const stars = [];
    const numStars = 200; // Adjust number of stars

    for (let i = 0; i < numStars; i++) {
        stars.push({
            x: Math.random() * canvas.width, // Random X position
            y: Math.random() * canvas.height, // Random Y position
            radius: Math.random() * 2 + 1, // Random size (1-3px)
            opacity: Math.random() * 0.8 + 0.2, // Random opacity (0.2-1)
        });
    }

    function drawStars() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = "#01072c"; // Deep blue background
        ctx.fillRect(0, 0, canvas.width, canvas.height);

        stars.forEach((star) => {
            ctx.beginPath();
            ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2);
            ctx.fillStyle = `rgba(62, 96, 242, ${star.opacity})`;
            ctx.fill();
        });
    }

    drawStars();

    // Twinkling effect (change opacity randomly)
    setInterval(() => {
        stars.forEach((star) => {
            star.opacity = Math.random() * 0.8 + 0.2;
        });
        drawStars();
    }, 1000);
});
</script>

<template>
    <canvas id="starryCanvas"></canvas>
</template>

<style scoped>
canvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    display: block;
}
</style>
