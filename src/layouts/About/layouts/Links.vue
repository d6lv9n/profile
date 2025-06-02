<template>
    <ul
    role="list"
    class="flex flex-grow flex-shrink gap-x-3 items-center pt-6
    sm:gap-x-6">
        <li>
            <a
            href="javascript:void(0);"
            title="Let's work together on Github!"
            class="bg-gray-800 border-2 border-gray-400 flex flex-grow-0 flex-shrink-0 items-center justify-center rounded-full size-10
            sm:size-14">
                <IconMDIGithub
                :height="iconSize"
                :width="iconSize"
                :color="'rgb(212, 212, 212)'"></IconMDIGithub>
            </a>
        </li>
        <li>
            <a
            href="javascript:void(0);"
            title="Let's connect on LinkedIn!"
            class="bg-gray-800 border-2 border-gray-400 flex flex-grow-0 flex-shrink-0 items-center justify-center rounded-full size-10
            sm:size-14">
                <IconMDILinkedin
                :height="iconSize"
                :width="iconSize"
                :color="'rgb(212, 212, 212)'"></IconMDILinkedin>
            </a>
        </li>
    </ul>
</template>

<script setup>
import { computed, onBeforeUnmount, onMounted, ref, watch } from 'vue';
// Icons
import IconMDIGithub from '@/svg-icons/mdi/github.vue';
import IconMDILinkedin from '@/svg-icons/mdi/linkedin.vue';

// Computed
const iconSize = computed(() => windowWidth.value < 640 ? 24 : 36);

// Data
const windowWidth = ref(0);

// Methods
function trackWindowWidth(event)
{
    windowWidth.value = event.target.innerWidth;
};

// Lifecycles
onMounted(() => {
    windowWidth.value = window.innerWidth;

    window.addEventListener('resize', trackWindowWidth);
});
onBeforeUnmount(() => {
    window.removeEventListener('resize', trackWindowWidth);
});
</script>
