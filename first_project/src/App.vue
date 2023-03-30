<template>
  <h1> {{title}}</h1>

</template>
<script setup>
  // life cycle hooks

import { onBeforeMount, onMounted, ref } from 'vue';
 let title = ref('')

  onBeforeMount(()=>{
    title.value= 'New Value'
    console.log('Before Mount');
  })

  onMounted(()=>{
    title.value= 'Vue js master Class'
    console.log(' Mounted');
  })
</script>