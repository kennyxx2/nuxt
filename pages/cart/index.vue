<script setup lang="ts">
const route = useRoute();

</script>

<template>
<div>{{ route.name }}</div>
<<NuxtLink to="/">Back</NuxtLink>

</template>

<style scoped>

</style>