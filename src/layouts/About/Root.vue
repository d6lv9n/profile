<template>
    <div class="relative w-full">
        <div class="bg-transparent flex flex-col pt-3 rounded-lg w-full
        sm:pt-6">
            <span class="font-bold text-2xl
            sm:text-4xl">Hi, my name is</span>

            <h1
            id="about"
            class="font-bold pt-1.5 scroll-pt-12 text-3xl
            sm:pt-3 sm:text-6xl">Christian Delvianto</h1>

            <LinksLayout></LinksLayout>

            <div class="pt-6
            lg:max-w-sm">
                <!-- Avatar -->
                <!-- <div class="bg-red-600 flex flex-grow-0 flex-shrink-0 items-center justify-center mx-auto overflow-hidden pb-6 rounded-full size-60
                lg:absolute lg:bottom-0 lg:right-0">
                    <img
                    src="../../../public/avatar.png"
                    class="object-contain size-full">
                </div> -->

                <span class="border-b-2 border-gray-400 pb-1.5 px-3">
                    <span class="font-bold text-gray-400 text-lg
                    sm:text-2xl">About</span>
                </span>

                <p class="pt-6 text-lg
                sm:text-2xl">I am a Full-Stack Web Developer, with experience hands-on building Single Page Application (SPA).</p>
            </div>
        </div>
    </div>
</template>

<script setup>
import LinksLayout from './layouts/Links.vue';
</script>