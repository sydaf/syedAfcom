<script setup>
import ProjectTag from "../ProjectTag.vue";
import ArrowIcon from "../Arrow.vue";
</script>

<template>
  <div
    class="panel panel-cvd md:row-span-2 md:col-span-4 md:order-4 order-9 relative flex flex-col justify-between"
  >
    <!-- <div class="absolute top-3 right-3">
            <ArrowIcon :showText="false"/>
          </div> -->
    <div class="flex items-center gap-1">
      <div class="absolute top-3 right-3">
        <a target="_blank" href="https://www.curriculum-vidae.com/">
          <ArrowIcon :showText="false" />
        </a>
      </div>
      <h2>CVD</h2>
    </div>
    <p>
      An app for creating video resume equipped with AI generated scripts and
      teleprompter
    </p>
    <div class="flex flex-wrap gap-1">
      <ProjectTag text="react-native" />
      <ProjectTag text="vueJs" />
      <ProjectTag text="ios" />
      <ProjectTag text="expo" />
      <ProjectTag text="android" />
      <ProjectTag text="typescript" />
    </div>
  </div>

  <div
    class="panel panel-naati md:row-span-2 md:col-span-4 md:order-5 order-10 relative flex flex-col justify-between"
  >
    <div class="absolute top-3 right-3">
      <a target="_blank" href="https://www.naati.com.au">
        <ArrowIcon :showText="false" />
      </a>
    </div>
    <h2>NAATI</h2>
    <p>Website refresh for translators and interpreters in Australia, using Elementor for easy customization.</p>
    <div class="flex flex-wrap gap-1">
      <ProjectTag text="custom-widget" />
      <ProjectTag text="custom-plugin" />
      <ProjectTag text="elementor" />
      <ProjectTag text="wordpress" />
    </div>
  </div>

  <div
    class="panel panel-osky md:row-span-2 md:col-span-4 md:order-8 order-11 flex flex-col justify-between relative"
  >
    <div class="absolute top-3 right-3">
      <a target="_blank" href="https://www.osky.com.au">
        <ArrowIcon :showText="false" />
      </a>
    </div>
    <h2>OSKY</h2>
    <p>Revamped the website for a leading Australian web development studio, enhancing design and functionality.</p>
    <div class="flex flex-wrap gap-1">
      <ProjectTag text="wordpress" />
      <ProjectTag text="bootstrap" />
      <ProjectTag text="jquery" />
      <ProjectTag text="cms" />
    </div>
  </div>

  <div
    class="panel panel-atoda md:row-span-2 md:col-span-4 order-12 flex flex-col justify-between relative"
  >
    <div class="absolute top-3 right-3">
      <a target="_blank" href="https://panaust.com.au/">
        <ArrowIcon :showText="false" />
      </a>
    </div>
    <h2>PANAUST</h2>
    <p>
      Revamped site for a copper and gold producer using WordPress CMS.
    </p>
    <div class="flex flex-wrap gap-1">
      <ProjectTag text="wordpress" />
      <ProjectTag text="bootstrap" />
      <ProjectTag text="jquery" />
      <ProjectTag text="cms" />
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectSection",
};
</script>
