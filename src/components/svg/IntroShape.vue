<template>
    <svg class="spinner bg-shapes" width="45" height="45" viewBox="0 0 45 45" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
            d="M25 0H20V16.4645L8.35786 4.82233L4.82233 8.35787L16.4645 20H0V25H16.4645L4.82233 36.6421L8.35787 40.1777L20 28.5355V45H25V28.5355L36.6421 40.1777L40.1777 36.6421L28.5355 25H45V20H28.5355L40.1777 8.35786L36.6421 4.82233L25 16.4645V0Z" />
    </svg>
</template>
  
<script>
export default {
    name: 'IntroShape',
};
</script>

<style>
.spinner {
    animation: spin 10s linear infinite;
}

@keyframes spin {
    0% {
        transform: rotate(0deg);
    }

    100% {
        transform: rotate(360deg);
    }
}
</style>