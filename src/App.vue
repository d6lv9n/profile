<template>
  <NavigationLayout></NavigationLayout>

  <div class="px-3 relative w-full
  lg:max-w-6xl lg:mx-auto lg:px-6">
    <AboutLayout></AboutLayout>

    <SkillsLayout></SkillsLayout>
  </div>

  <Transition appear mode="out-in" name="fade">
    <WelcomeModal
    v-if="modals.welcome"
    @close="modals.welcome = false"></WelcomeModal>
  </Transition>
</template>

<script setup>
import { onBeforeMount, onMounted, reactive } from 'vue';
// Layouts
import AboutLayout from './layouts/About/Root.vue';
import NavigationLayout from './layouts/Navigation.vue';
import SkillsLayout from './layouts/Skills/Root.vue';
// Modals
import WelcomeModal from './modals/Welcome/Root.vue';

// Data
const modals = reactive({
  welcome: false,
});

// Lifecycles
onBeforeMount(() => {
  // Check if the welcome modal should be shown
  if (! localStorage.getItem('hasVisited') && ! localStorage.getItem('visitTime')) {
    modals.welcome = true;

    localStorage.setItem('hasVisited', 'true');
    localStorage.setItem('visitTime', new Date().toISOString());
  }
});
</script>