<template>
    <div class="flex items-center space-x-2">
        <div class="text-gray-500 text-xs" v-if="showNextMode">Change to {{ nextMode }}</div>
        <button @click="toggleColorMode" @mouseenter="showNextMode = true" @mouseleave="showNextMode = false" class="hover:bg-gray-200 dark:hover:bg-gray-600 px-2 py-1 rounded-lg">{{ nextModeIcon }}</button>
    </div>
</template>
<script setup>
const showNextMode = ref(false);
const colorMode = useColorMode();

const modes = ['system', 'light', 'dark'];

const nextModeIcons = {
    system: '🌓',
    light: '🌕',
    dark: '🌑'
}

const nextMode = computed(() => {
    const currentIndex = modes.indexOf(colorMode.preference);
    const nextIndex = (currentIndex + 1) % modes.length;
    return modes[nextIndex];
});

const nextModeIcon = computed(() => nextModeIcons[nextMode.value]);

const toggleColorMode = () => colorMode.preference = nextMode.value;
</script>