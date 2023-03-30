<template>
  <h1 v-show="showBtn">{{courseName}}</h1>
  <p>{{ student }}</p>
  <button @click="showBtn=!showBtn">show/hide</button>
<br>
<input type="number" v-model="count">
<div>
  <button @click="increment(1)"> + </button>
      <h2>  {{ count }} / {{checkOddEven }}</h2>
  <button @click="decrement(1)"> - </button>
</div>
</template>
<script setup>
   import {computed, ref, watch} from 'vue';
   let count = ref(0);
   let showBtn= ref(false)
   const checkOddEven  = computed(()=>{
     return count.value %2 === 0 ? 'even': 'odd';
   })
    const  courseName = ref("Vue js  Master Class");
    const   student = ref("rasbappy");

    /* Methods*/
 const increment = amount=> count.value += amount;
 const decrement = amount=> count.value -= amount;


    // watch
  watch (()=> count.value, (newValue, oldValue)=> {
    console.log('newValue', newValue);
    console.log('oldValue', oldValue);
    if (newValue>10) {
      alert('Counter value  is over tha 10')
    }
  })
</script>