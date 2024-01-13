<script setup>
import { ref } from 'vue';
import DarkModeIcon from './components/svg/darkMode.vue';
import LightModeIcon from './components/svg/lightMode.vue';

let dark = ref(false);

const toggleDarkMode = () => {
  dark.value = !dark.value;
};
</script>

<template>
  <div class="bg-container max-h-screen" :class="{ 'dark-mode': dark, 'light-mode': !dark }">
    <div class="max-w-5xl">
      <div class="mode-toggler flex">
        <transition name="icon-spin" mode="out-in">
          <DarkModeIcon v-if="dark" key="dark-mode-icon" />
          <LightModeIcon v-else key="light-mode-icon" />
        </transition>
        <button @click="toggleDarkMode">Toggle {{ dark ? 'Dark' : 'Light' }} Mode</button>
      </div>
    </div>
  </div>
</template>