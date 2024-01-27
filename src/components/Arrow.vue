<template>
  <button class="flex flex-col gap-0.5 items-center arrow-icon">
    <svg class="changeable-svg" width="22" height="22" viewBox="0 0 22 22" fill="none" xmlns="http://www.w3.org/2000/svg">
      <path class="changeable-path" fill-rule="evenodd" clip-rule="evenodd"
        d="M0.604092 21.3959C1.40955 22.2014 2.71545 22.2014 3.52091 21.3959L17.875 7.04182L17.875 17.1875C17.875 18.3266 18.7984 19.25 19.9375 19.25C21.0766 19.25 22 18.3266 22 17.1875L22 2.0625C22 0.923413 21.0766 2.51336e-07 19.9375 2.37752e-07L4.8125 5.73885e-08C3.67341 4.3805e-08 2.75 0.923412 2.75 2.0625C2.75 3.20159 3.67341 4.125 4.8125 4.125L14.9582 4.125L0.604092 18.4791C-0.201364 19.2845 -0.201364 20.5905 0.604092 21.3959Z" />
    </svg>
    <p v-if="showText" class="p-bold text-xs transition-transform">more!</p>
  </button>
</template>
  
<script>
export default {
  name: 'ArrowIcon',
  props: {
    showText: {
      type: Boolean,
      default: true,
    },
  },
};
</script>

<style lang="scss">
.dark-mode {

  .arrow-icon {
    transition: all 150ms ease-in-out;

    &:hover .transition-transform {
      transform: translateY(3px);
    }

    &:hover .changeable-path {
      opacity: 0.6;
    }
  }
}

.light-mode {

  .arrow-icon {
    transition: all 150ms ease-in-out;

    &:hover .transition-transform {
      transform: translateY(3px);
    }

    &:hover .changeable-path {
      opacity: 0.5;
    }
  }
}
</style>