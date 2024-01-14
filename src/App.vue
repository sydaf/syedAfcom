<script setup>
import { ref } from 'vue';
import DarkModeIcon from './components/svg/DarkMode.vue';
import LightModeIcon from './components/svg/LightMode.vue';
import ButtonPrimary from './components/ButtonPrimary.vue';
import IntroShape from './components/svg/IntroShape.vue';
import ArrowIcon from './components/svg/Arrow.vue';
import StarBig from './components/svg/StarBig.vue';
import StarSmall from './components/svg/StarSmall.vue';
import QuestionMark from './components/svg/QuestionMark.vue';

let dark = ref(false);

const toggleDarkMode = () => {
  dark.value = !dark.value;
};

const currentYear = ref(new Date().getFullYear());
</script>

<template>
  <div
    class="bg-container md:max-h-screen md:h-screen flex items-center justify-center px-1.5 md:px-0 selection:bg-lime-400 selection:text-slate-950"
    :class="{ 'dark-mode': dark, 'light-mode': !dark }">
    <div class="max-w-4xl">

      <!-- Heading -->
      <div class="grid md:grid-rows-1 md:grid-cols-10 gap-0.5">
        <div class="mode-toggler flex items-end gap-2 md:row-span-1 md:col-span-6 order-first">
          <button class="mode-toggle-btn flex gap-2 items-center" @click="toggleDarkMode">
            <transition name="icon-spin" mode="out-in">
              <LightModeIcon v-if="dark" key="light-mode-icon" />
              <DarkModeIcon v-else key="dark-mode-icon" />
            </transition>
            <p>Too {{ dark ? 'Dark' : 'Bright' }}?</p>
          </button>
        </div>
        <div class="md:row-span-1 md:col-span-4 md:order-1 hidden md:block order-8">
          <h1>Selected work</h1>
        </div>
      </div>

      <!-- Content -->
      <div class="gap-color p-0.5 grid md:grid-rows-8 md:grid-cols-10 gap-0.5">
        <img class="round-custom md:row-span-3 md:col-span-3 order-2 object-cover md:object-none" src="./assets/img/sydimg.webp"
          alt="A picture of this creature of a developer">

        <div
          class="panel panel-intro md:row-span-3 md:col-span-3 md:order-3 order-1 flex flex-col justify-between relative">
          <h1>Hello! <span class="hand-wave">🖐️</span> I'm Syed.</h1>
          <p>A fellow front-end developer building passion-driven user interfaces to bring your digital experiences to
            life.</p>
          <ButtonPrimary buttonText="resume'"></ButtonPrimary>
          <IntroShape class="absolute bottom-2 right-2" />
        </div>

        <div
          class="panel panel-about md:row-span-2 md:col-span-4 md:order-6 order-3 flex justify-between flex-col relative">
          <h2 class="text-xl">About.</h2>
          <p>
            I’m currently working as a front-end developer at Osky Interactive. Mainly working a lot with Wordpress
            templates and headless CMS.
          </p>
          <div class="absolute top-2 right-2">
            <ArrowIcon />
          </div>
          <div class="absolute right-0">
            <StarSmall />
          </div>
          <div class="absolute right-0">
            <StarBig />
          </div>
        </div>

        <div class="panel panel-mystery md:row-span-2 md:col-span-2 md:order-7 order-4 flex justify-center items-center">
          <QuestionMark/>
        </div>
        <div class="panel md:row-span-3 md:col-span-3 md:order-9 order-5">contact</div>
        <div class="panel md:row-span-1 md:col-span-3 md:order-10 order-6">tech stack</div>
        <div class="panel md:row-span-2 md:col-span-3 md:order-11 order-7">experience</div>

        <!-- Projects -->
        <div class="md:row-span-1 md:col-span-4 md:order-1 md:hidden block order-8">prjt</div>
        <div class="panel md:row-span-2 md:col-span-4 md:order-4 order-9">project1</div>
        <div class="panel md:row-span-2 md:col-span-4 md:order-5 order-10">project2</div>
        <div class="panel md:row-span-2 md:col-span-4 md:order-8 order-11">project3</div>
        <div class="panel md:row-span-2 md:col-span-4 order-12">project4</div>
      </div>

      <!-- Footer -->
      <div class="md:row-span-1 md:col-span-10 order-last text-center flex justify-center mt-5 ">
        <p class="max-w-[225px]">© {{ currentYear }} · Crafted with ❤️ using Tailwind and Vue.js</p>
      </div>

    </div>
  </div>
</template>