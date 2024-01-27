<script setup>
import IntroShape from '../svg/IntroShape.vue';
import ButtonPrimary from '../ButtonPrimary.vue';
</script>

<template>
    <div
        class="panel panel-intro md:row-span-3 md:col-span-3 md:order-3 order-1 flex flex-col gap-3 md:gap-0 md:justify-between relative">
        <h1>Hello! <span class="hand-wave">🖐️</span> <br> I'm Syed.</h1>
        <p>A fellow front-end developer building passion-driven user interfaces to bring your digital experiences to
            life.</p>
        <a href="SyedAF.pdf" target="_blank" type="application/pdf" rel="alternate" media="print">
            <ButtonPrimary buttonText="resume'"></ButtonPrimary>
        </a>
        <IntroShape class="absolute bottom-2 right-2 pointer-events-none" />
    </div>
</template>

<script>
export default {
    name: 'IntroSection',
};
</script>

<style lang="scss">
//==== Transition ====//
.icon-spin-enter-active,
.icon-spin-leave-active {
    transition: all 250ms ease-in-out !important;
}

.icon-spin-enter,
.icon-spin-leave-to {
    transform: rotate(360deg);
    transform-origin: center;
    opacity: 0;
}

@keyframes wave {
    0% {
        transform: rotate(0.0deg)
    }

    10% {
        transform: rotate(14.0deg)
    }

    /* The following five values can be played with to make the waving more or less extreme */
    20% {
        transform: rotate(-8.0deg)
    }

    30% {
        transform: rotate(14.0deg)
    }

    40% {
        transform: rotate(-4.0deg)
    }

    50% {
        transform: rotate(10.0deg)
    }

    60% {
        transform: rotate(0.0deg)
    }

    100% {
        transform: rotate(0.0deg)
    }
}

.hand-wave {
    display: inline-block;
    animation: wave 2s infinite;
}
</style>
