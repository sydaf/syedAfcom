<template>
    <button class="button-primary round-custom text-xl px-5 py-1.5 w-fit">{{ buttonText }}</button>
</template>

<script>
export default {
    name: 'ButtonPrimary',
    props: {
        buttonText: {
            type: String,
            default: 'Click me',
        },
    },
};
</script>
