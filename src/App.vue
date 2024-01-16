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
import PhoneIcon from './components/svg/Phone.vue';
import EnvelopIcon from './components/svg/Envelop.vue';
import DiscordIcon from './components/svg/Discord.vue';
import GithubIcon from './components/svg/Github.vue';
import LinkedinIcon from './components/svg/Linkedin.vue';
import GlobeShape from './components/svg/GlobeShape.vue';
import ProjectTag from './components/ProjectTag.vue';

import Bootstrap from './components/svg/Bootstrap.vue';
import Git from './components/svg/Git.vue';
import JavaScript from './components/svg/JavaScript.vue';
import Jquery from './components/svg/Jquery.vue';
import ReactJs from './components/svg/ReactJs.vue';
import Sass from './components/svg/Sass.vue';
import TwScss from './components/svg/TwScss.vue';
import VueIcon from './components/svg/VueIcon.vue';
import Wordpress from './components/svg/Wordpress.vue';
import Yarn from './components/svg/Yarn.vue';

import { Vue3Marquee } from 'vue3-marquee'

let dark = ref(false);

const toggleDarkMode = () => {
  dark.value = !dark.value;
};

const currentYear = ref(new Date().getFullYear());

const imgArray = [
  'https://sponsors.vuejs.org/images/vueschool.avif',
  'https://sponsors.vuejs.org/images/vehikl.avif',
  'https://sponsors.vuejs.org/images/vehikl.avif',
  'https://sponsors.vuejs.org/images/vehikl.avif',
  'https://sponsors.vuejs.org/images/dronahq.avif',
];
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
        <img class="round-custom md:row-span-3 md:col-span-3 order-2 object-cover md:object-none w-full "
          src="./assets/img/sydimg.webp" alt="A picture of this creature of a developer">

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
          <div class="absolute top-3 right-3">
            <ArrowIcon />
          </div>
          <div class="absolute right-24 top-0">
            <StarSmall />
          </div>
          <div class="absolute right-0">
            <StarBig />
          </div>
        </div>

        <div class="panel panel-mystery md:row-span-2 md:col-span-2 md:order-7 order-4 flex justify-center items-center">
          <QuestionMark />
        </div>

        <div class="panel panel-contact md:row-span-3 md:col-span-3 md:order-9 order-5 flex flex-col gap-2">
          <h2 class="text-xl">Contact.</h2>
          <div class="flex items-center gap-2">
            <PhoneIcon />
            <a href="#">016-234 5965</a>
          </div>
          <div class="flex items-center gap-2">
            <EnvelopIcon />
            <a href="#">syedafinquiries</a>
          </div>
          <h2 class="text-xl">Socials.</h2>
          <div class="flex items-center gap-3">
            <a href="#">
              <GithubIcon />
            </a>
            <a href="#">
              <DiscordIcon />
            </a>
            <a href="#">
              <LinkedinIcon />
            </a>
          </div>
        </div>

        <div class="panel panel-stack md:row-span-1 md:col-span-3 md:order-10 order-6 flex items-center relative">
          <Vue3Marquee :clone="true" :duration="20" :pause-on-hover="true">
            <Bootstrap />
            <Git />
            <JavaScript />
            <Jquery />
            <ReactJs />
            <Sass />
            <TwScss />
            <VueIcon />
            <Wordpress />
            <Yarn />
          </Vue3Marquee>
        </div>

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

        <!-- Projects -->
        <div class="md:row-span-1 md:col-span-4 md:order-1 md:hidden block order-8 text-center ">
          <h1 class="invert-mode py-5 ">Selected work</h1>
        </div>

        <div
          class="panel panel-cvd md:row-span-2 md:col-span-4 md:order-4 order-9 relative flex flex-col justify-between">
          <div class="absolute top-3 right-3">
            <ArrowIcon :showText="false" />
          </div>
          <h2>CVD</h2>
          <p>An app for creating video resume equipped with AI generated scripts and teleprompter</p>
          <div class="flex flex-wrap gap-1">
            <ProjectTag text="react-native" />
            <ProjectTag text="vueJs" />
            <ProjectTag text="ios" />
            <ProjectTag text="expo" />
            <ProjectTag text="app development" />
            <ProjectTag text="typescript" />
          </div>
        </div>

        <div
          class="panel panel-naati md:row-span-2 md:col-span-4 md:order-5 order-10 relative flex flex-col justify-between">
          <div class="absolute top-3 right-3">
            <ArrowIcon :showText="false" />
          </div>
          <h2>NAATI</h2>
          <p>Website revamp for translators and interpreters in Australia.</p>
          <div class="flex flex-wrap gap-1">
            <ProjectTag text="custom-widget" />
            <ProjectTag text="custom-plugin" />
            <ProjectTag text="elementor" />
            <ProjectTag text="wordpress" />
            <ProjectTag text="jquery" />
            <ProjectTag text="cms" />
          </div>
        </div>
        <div
          class="panel panel-osky md:row-span-2 md:col-span-4 md:order-8 order-11 flex flex-col justify-between relative">
          <div class="absolute top-3 right-3">
            <ArrowIcon :showText="false" />
          </div>
          <h2>OSKY</h2>
          <p>Website revamp for a web development studio in Canberra Australia.</p>
          <div class="flex flex-wrap gap-1">
            <ProjectTag text="wordpress" />
            <ProjectTag text="bootstrap" />
            <ProjectTag text="jquery" />
            <ProjectTag text="cms" />
          </div>
        </div>
        <div class="panel panel-atoda md:row-span-2 md:col-span-4 order-12 flex flex-col justify-between relative">
          <div class="absolute top-3 right-3">
            <ArrowIcon :showText="false" />
          </div>
          <h2>ATODA</h2>
          <p>Website revamp for a registered not-for-profit organisation with the Australian Charities and Not-for-profits
            Commission</p>
          <div class="flex flex-wrap gap-1">
            <ProjectTag text="wordpress" />
            <ProjectTag text="bootstrap" />
            <ProjectTag text="jquery" />
            <ProjectTag text="cms" />
          </div>
        </div>
      </div>

      <!-- Footer -->
      <div class="md:row-span-1 md:col-span-10 order-last text-center flex justify-center mt-5 mb-5 md:mb-0">
        <p class="max-w-[225px]">© {{ currentYear }} · Assembled with ❤️ using Tailwind and Vue.js</p>
      </div>

    </div>
  </div>
</template>