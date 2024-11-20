<script setup lang="ts">
import spinner from './components/spinner.vue';
import DataKeys from './constants/DataKeys';


const { data, pending, refresh }= await useFetch('https://dummyjson.com/products?limit=10' ,{
  immediate: false,
  key: DataKeys.PRODUCTS,
    });
  onMounted(()=>{
    refresh();
  })
</script>
<template>
  <div>
    <Spinner v-if="pending"/>
    <NuxtLayout v-else>
    
    <NuxtPage />
    </NuxtLayout>
  </div>
</template>