<script setup>
import { Vue3Marquee } from 'vue3-marquee'

import Bootstrap from '../svg/Bootstrap.vue';
import Git from '../svg/Git.vue';
import JavaScript from '../svg/JavaScript.vue';
import Jquery from '../svg/Jquery.vue';
import ReactJs from '../svg/ReactJs.vue';
import Sass from '../svg/Sass.vue';
import TwScss from '../svg/TwScss.vue';
import VueIcon from '../svg/VueIcon.vue';
import Wordpress from '../svg/Wordpress.vue';
import Yarn from '../svg/Yarn.vue';
import Gpql from '../svg/Gpql.vue';
import Nextjs from '../svg/Nextjs.vue';
import Redux from '../svg/Redux.vue';
</script>

<template>
    <div class="panel panel-stack md:row-span-1 md:col-span-3 md:order-10 order-6 flex items-center relative">
        <Vue3Marquee :clone="true" :duration="20" :pause-on-hover="true">
            <Bootstrap />
            <Redux />
            <Git />
            <JavaScript />
            <Jquery />
            <ReactJs />
            <Sass />
            <TwScss />
            <VueIcon />
            <Wordpress />
            <Yarn />
            <Gpql />
            <Nextjs />
        </Vue3Marquee>
    </div>
</template>

<script>
export default {
    name: 'StackSection',
};
</script>