<template>
  <NavigationLayout></NavigationLayout>

  <div class="px-3 relative w-full
  lg:max-w-6xl lg:mx-auto lg:px-6">
    <AboutLayout></AboutLayout>

    <SkillsLayout></SkillsLayout>
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
// Layouts
import AboutLayout from './layouts/About/Root.vue';
import NavigationLayout from './layouts/Navigation.vue';
import SkillsLayout from './layouts/Skills/Root.vue';
</script>