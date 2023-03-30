<template>
  <h1> {{title}}</h1>

</template>
<script setup>
  // life cycle hooks

import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated, ref } from 'vue';
 let title = ref('')

  onBeforeMount(()=>{
    title.value= 'New Value'
    console.log('Before Mount');
  })

  onMounted(()=>{
    title.value= 'Vue js master Class'
    console.log(' Mounted');
  })
  onUpdated (()=>{ 
    console.log(' upateded');
  })

  onBeforeUpdate(()=>{
    console.log('before upateded');
  })
  onBeforeUnmount(()=> {
    console.log('before unmount');
  })
  onUnmounted (()=>{
    console.log('unmounted');
  })


</script>