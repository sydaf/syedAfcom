<script setup>
import { ref } from 'vue';
import DarkModeIcon from './components/svg/DarkMode.vue';
import LightModeIcon from './components/svg/LightMode.vue';
import QuestionMark from './components/svg/QuestionMark.vue';

import IntroSection from './components/sections/introSection.vue';
import AboutSection from './components/sections/aboutSection.vue';
import ContactSection from './components/sections/contactSection.vue';
import StackSection from './components/sections/stackSection.vue';
import ExpSection from './components/sections/expSection.vue';
import ProjectSection from './components/sections/projectSection.vue';

let dark = ref(false)
let primaryAbt = ref(true)

const toggleDarkMode = () => {
  dark.value = !dark.value;
};

const togglePersonal = () => {
  primaryAbt.value = !primaryAbt.value
}

const currentYear = ref(new Date().getFullYear());
</script>

<template>
  <div
    class="bg-container flex min-h-screen items-center justify-center px-1.5 md:px-0 py-3 md:py-4 selection:bg-lime-400 selection:text-slate-950"
    :class="{ 'dark-mode': dark, 'light-mode': !dark }">
    <div class="max-w-4xl">

      <!-- Heading -->
      <div class="grid md:grid-rows-1 md:grid-cols-10 gap-0.5">
        <div
          class="mode-toggler flex items-end gap-2 md:row-span-1 md:col-span-6 order-first justify-center md:justify-start">
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
        <img class="round-custom md:row-span-3 md:col-span-3 order-2 object-cover md:object-none w-full relative z-1"
          src="./assets/img/sydimg.webp" alt="A picture of this creature of a developer">

        <IntroSection />
        <AboutSection />

        <div class="panel panel-mystery md:row-span-2 md:col-span-2 md:order-7 order-4 flex justify-center items-center">
          <QuestionMark />
        </div>

        <ContactSection />
        <StackSection />
        <ExpSection />

        <!-- Projects -->
        <div class="md:row-span-1 md:col-span-4 md:order-1 md:hidden block order-8 text-center ">
          <h1 class="invert-mode py-5 ">Selected work</h1>
        </div>

        <ProjectSection />

      </div>

      <!-- Footer -->
      <div class="md:row-span-1 md:col-span-10 order-last text-center flex justify-center mt-5 mb-5 md:mb-0">
        <p class="max-w-[225px]">© {{ currentYear }} · Assembled with ❤️ using <a target="_blank" class="p-bold"
            href="https://tailwindcss.com">Tailwind</a> and <a target="_blank" class="p-bold"
            href="https://vuejs.org">VueJs</a> <br>
            Hosted by <a class="p-bold" href="https://aliifz,.com">AliifZin</a>
          </p>
      </div>

    </div>
  </div>
</template>