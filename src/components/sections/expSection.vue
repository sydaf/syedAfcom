<script setup>
import GlobeShape from '../svg/GlobeShape.vue';
</script>

<template>
    <div class="panel panel-exp md:row-span-2 md:col-span-3 md:order-11 order-7 flex flex-col gap-2 relative">
        <h2 class="text-xl">Experience.</h2>
        <div class="first-exp">
            <p>OSKY Interactive</p>
            <p class="opacity-60">2023 - Present</p>
        </div>
        <div class="second-exp">
            <p>Sfera Digital Solutions</p>
            <p class="opacity-60">2020 - 2022</p>
        </div>
        <div class="absolute right-0 bottom-0">
            <GlobeShape />
        </div>
    </div>
</template>

<script>
export default {
    name: 'ExpSection',
}
</script>

<style lang="scss">
.globe-shape {
    animation: pulsing 5s ease-in-out infinite;
}

@keyframes pulsing {
    0% {
        transform: scale(0.95);
    }

    70% {
        transform: scale(1);
    }

    100% {
        transform: scale(0.95);
    }
}
</style>