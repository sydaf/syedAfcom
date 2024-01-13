<script setup>
  let dark = true;

  const toggleDarkMode = () => {
    dark = !dark;
  };
</script>

<template>
  <button @click="toggleDarkMode">Toggle Dark Mode</button>
  <h1 class="text-3xl font-bold underline">
    Dark Mode: {{ dark ? 'Enabled' : 'Disabled' }}
  </h1>
</template>