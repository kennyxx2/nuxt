<script setup lang="ts">
import DataKeys from '~/constants/DataKeys';

const route = useRoute();
const {data} = useNuxtData(DataKeys.PRODUCTS)

</script>

<template>
<div class="grid grid-cols-4 gap-2 place-content-start">

<div v-for="product in data.products" :key="product.id" class="h-full w-full">
    <div class="card  bg-base-100 w-96 shadow-xl  h-full w-full" >
  <figure>
    <img
      :src="product.thumbnail"
      alt="Shoes" />
  </figure>
  <div class="card-body">
    <h2 class="card-title"> {{ product.title }}</h2>
    <p>{{ product.description }}</p>
    <div class="card-actions justify-end">
      <button class="btn btn-primary">Buy Now</button>
    </div>
  </div>
</div>
</div>
</div>
</template>

<style scoped>

</style>