<script setup>
import Land from './Land/Land.vue';
import Land2 from './Land/Land2.vue';
import Land3 from './Land/Land3.vue';
import Land4 from './Land/Land4.vue';
import Land5 from './Land/Land5.vue';
import Land6 from './Land/Land6.vue';
import Land7 from './Land/Land7.vue';
</script>

<template>
    <div class="relative flex items-center justify-center rounded-full bg-[#000c39] size-[calc(100vh-10rem)]">
        <div
            class="relative flex items-center justify-center rounded-full bg-[rgba(1,23,79,0.5)] size-[calc(100vh-14rem)]">
            <div class="relative flex items-center justify-center rounded-full bg-[#012573] size-[calc(100vh-18rem)]">
                <div
                    class="relative flex items-center justify-center rounded-full bg-[#06164b] size-[calc(100vh-22rem)]">
                    <div
                        class="absolute flex items-center justify-center size-[calc(100vh-25rem)] rounded-full overflow-hidden">
                        <Land />
                        <Land7 class="top-24 right-[550px]" />
                        <Land2 class="top-0 left-10" />
                        <Land3 class="bottom-20 right-[300px]" />
                        <Land3 class="bottom-0 right-30" />
                        <Land4 class="bottom-10 left-15" />
                        <Land5 class="bottom-15 right-64" />
                        <Land6 class="top-10 right-72" />
                        <div class="absolute inset-0 bg-[#218cd7] rounded-full"></div>
                        <div class="absolute inset-0 bg-black/25 rounded-full clip-half-circle z-20"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.clip-half-circle {
    clip-path: polygon(50% 0, 100% 0, 100% 100%, 50% 100%);
}
</style>
