<script setup>
import PhoneIcon from '../svg/Phone.vue';
import EnvelopIcon from '../svg/Envelop.vue';
import DiscordIcon from '../svg/Discord.vue';
import GithubIcon from '../svg/Github.vue';
import LinkedinIcon from '../svg/Linkedin.vue';
</script>

<template>
    <div class="panel panel-contact md:row-span-3 md:col-span-3 md:order-9 order-5 flex flex-col gap-3 md:gap-2">
        <h2 class="text-xl">Contact.</h2>
        <div class="flex items-center gap-2">
            <PhoneIcon />
            <div class="relative">
                <a class="slider-link" target="_blank" href="https://wa.me/60162435965">016-234 5965</a>
            </div>
        </div>
        <div class="flex items-center gap-2">
            <EnvelopIcon />
            <div class="relative">
                <a class="slider-link" href="mailto:syedahmadfakhrullah@gmail.com">syedahmadfakhrullah</a>
            </div>
        </div>
        <h2 class="text-xl">Socials.</h2>
        <div class="flex items-center gap-3">
            <a target="_blank" href="https://github.com/sydaf/">
                <GithubIcon />
            </a>
            <a target="_blank" href="discordapp.com/users/612376608745193513">
                <DiscordIcon />
            </a>
            <a target="_blank" href="https://www.linkedin.com/in/fakrulfauzi/">
                <LinkedinIcon />
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ContactSection',
};
</script>
