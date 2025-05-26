<template>
  <NavigationLayout></NavigationLayout>

  <div class="px-3 relative w-full
  lg:max-w-6xl lg:mx-auto lg:px-6">
    <AboutLayout></AboutLayout>

    
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
// Layouts
import AboutLayout from './components/About.vue';
import NavigationLayout from './components/Navigation.vue';
</script>