<template>
    <div class="py-0.5 px-1.5 project-tag rounded-full">
        <p>{{ text }}</p>
    </div>
</template>

<script>
export default {
  name: 'ProjectTag',
  props: {
    text: {
            type: String,
            default: 'web',
        },
  },
};
</script>