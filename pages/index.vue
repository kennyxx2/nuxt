<script setup lang="ts">
const route = useRoute();
const counter = ref(0)
definePageMeta({
    name:"Index"
})
</script>

<template>
    <div>{{ route.name }}</div>
    <Counter />
    
    <div>
    <<NuxtLink to="/cart">Cart</NuxtLink>
    <<NuxtLink to="/products">Products</NuxtLink>
    <<NuxtLink to="/users">Users</NuxtLink>
    </div>
    <details class="dropdown">
  <summary class="btn m-1">open or close</summary>
  <ul class="menu dropdown-content bg-base-100 rounded-box z-[1] w-52 p-2 shadow">
    <li><a>Item 1</a></li>
    <li><a>Item 2</a></li>
  </ul>
</details>
</template>

<style scoped>

</style>