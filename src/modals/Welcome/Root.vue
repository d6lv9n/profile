<template>
    <div class="bg-black/60 fixed flex items-center justify-center inset-0 p-6 size-full z-10
    sm:p-0">
        <button
        @click="close"
        type="button"
        class="absolute bg-transparent inset-0 select-none size-full text-transparent">&nbsp;</button>

        <Transition appear mode="out-in" name="scale">
            <div
            v-if="isMounted"
            class="bg-white flex flex-col gap-y-3 max-w-md p-6 relative rounded-xl w-full z-10">
                <img
                :src="welcomeImage"
                alt="Welcome"
                draggable="false"
                class="animate-pulse bg-black block rounded-lg"/>

                <p class="text-center text-gray-800">Hi welcome to my profile and I thank you for the visit, but unfortunately, <b>this page is still under progress</b>. Please kindly revisit again later.</p>

                <button
                @click="close"
                type="button"
                class="bg-blue-500 font-semibold py-1.5 rounded-full text-lg text-white
                focus:bg-blue-800
                hover:bg-blue-800">Understood</button>
            </div>
        </Transition>
    </div>
</template>

<script setup>
import { onBeforeUnmount, onMounted, ref } from 'vue';
// Images
import welcomeImage from '@/assets/images/Welcome.jpg';

// Data
const isMounted = ref(false);

// Emits
const emits = defineEmits([
    'close'
]);

// Methods
function close()
{
    if (! isMounted.value) {
        return;
    }

    isMounted.value = false;

    setTimeout(() => {
        emits('close');
    }, 300);
};

// Lifecycles
onMounted(() => {
    document.body.classList.add('overflow-hidden');

    isMounted.value = true;
});
onBeforeUnmount(() => {
    isMounted.value = false;

    document.body.classList.remove('overflow-hidden');
});
</script>