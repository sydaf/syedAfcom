<script setup>
import { ref } from 'vue';
import StarBig from '../svg/StarBig.vue';
import StarSmall from '../svg/StarSmall.vue';
import ArrowIcon from '../Arrow.vue';

let primaryAbt = ref(true)

const togglePersonal = () => {
    primaryAbt.value = !primaryAbt.value
}
</script>

<template>
    <div class="panel panel-about md:row-span-2 md:col-span-4 md:order-6 order-3 flex gap-3 md:gap-0 justify-between flex-col relative"
        :class="{ 'not-personal': primaryAbt, 'personal': !primaryAbt }">
        <h2 class="text-xl">About.</h2>
        <div v-if="primaryAbt" class="primary-abt">
            <p>
                I’m currently working as a front-end developer at Osky Interactive. Mainly working a lot with Wordpress
                templates and headless CMS.
            </p>
        </div>
        <div v-else class="personal-abt">
            <p class="pb-3 ">
                In my free time, I'm working on my photography skills and playing MMOs like <a target="_blank" class="p-bold" href="https://www.guildwars2.com">Guild Wars 2</a>.
            </p>
            <div class="flex gap-2 items-center">
                <img src="../../assets/img/untamed.png" alt="I play an Untamed">
                <img src="../../assets/img/mechanist.png" alt="I play a Mechanist">
                <p class="p-bold">syd.6418</p>
            </div>
        </div>
        <div class="absolute top-3 right-3">
            <ArrowIcon @click="togglePersonal" />
        </div>
        <div class="absolute right-24 top-0 pointer-events-none">
            <StarSmall :class="{ 'floating-sm': primaryAbt, 'floating-p': !primaryAbt }" />
        </div>
        <div class="absolute right-0 pointer-events-none">
            <StarBig :class="{ 'floating': primaryAbt, 'floating-p-sm': !primaryAbt }" />
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutSection',
};
</script>

<style lang="scss">
.slider-link {

    &::after {
        z-index: -1;
        opacity: 0;
        content: '';
        position: absolute;
        bottom: -1px;
        right: 0px;
        transition: all 0.3s ease;
        display: block;
        background: url(../../assets/img/hand-point.webp) no-repeat center center;
        background-size: cover;
        width: 20px;
        height: 20px;
    }

    &:hover::after {
        right: -30px;
        opacity: 1;
    }
}

.floating {
    animation: floating 3s ease-in-out infinite;
}

.floating-sm {
    animation: floating 3s ease-in-out infinite 500ms;
}

.floating-p {
    animation: floatingP 3s ease-in-out infinite;
}

.floating-p-sm {
    animation: floatingPSM 3500ms ease-in-out infinite;
}

@keyframes floatingP {
    0% {
        transform: translate(0, 0px) rotate(15deg);
    }

    50% {
        transform: translate(0, 15px) rotate(5deg);
    }

    100% {
        transform: translate(0, -0px) rotate(15deg);
    }
}

@keyframes floatingPSM {
    0% {
        transform: translate(0, 0px) rotate(-15deg);
    }

    50% {
        transform: translate(0, 15px) rotate(-5deg);
    }

    100% {
        transform: translate(0, -0px) rotate(-15deg);
    }
}

@keyframes floating {
    0% {
        transform: translate(0, 0px);
    }

    50% {
        transform: translate(0, 15px);
    }

    100% {
        transform: translate(0, -0px);
    }
}
</style>