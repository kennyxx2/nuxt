<template>
  
    <div class="flex flex row justify-center items-center">
         {{ counter }}
         <button @click="counter++">+</button>
    </div>
    
  
</template>

<script lang="ts" setup>
const counter = ref(0)
</script>

<style scoped>

</style>