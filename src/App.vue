<template>
  <div class="container" style="padding-top:60px">
    <h1>Compteur</h1>
    <p>
      Compteur {{ count }} x 2= {{ double }}
    </p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue';

const count = ref(0);
const double = computed(() => count.value *2);
const increment = () => count.value++;
</script>