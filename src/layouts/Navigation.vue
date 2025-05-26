<style scoped>
nav {
    @apply bg-gray-900/30 backdrop-blur-sm flex flex-grow flex-row flex-shrink items-center justify-between px-3 py-6 sticky top-0 w-full z-10
    lg:max-w-6xl lg:mx-auto lg:px-6;
}
</style>

<template>
    <nav>
        <button
        v-text="'<C/D>'"
        @click="scrollToTop"
        type="button"
        class="font-bold text-2xl
        sm:text-3xl"></button>

        <ul
        role="list"
        class="flex flex-grow-0 flex-grow flex-shrink-0 gap-x-3 items-centers
        sm:gap-x-6">
            <li>
                <a
                href="#about"
                class="font-semibold
                sm:text-lg">About</a>
            </li>
            <li>
                <a
                href="#project"
                class="font-semibold
                sm:text-lg">Projects</a>
            </li>
            <li>
                <a
                href="#contact"
                class="font-semibold
                sm:text-lg">Contact</a>
            </li>
        </ul>
    </nav>
</template>

<script setup>
// Methods
function scrollToTop()
{
    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    });
};
</script>