<template>
    <nav class="font-mono">
        <ul class="flex space-x-4">
            <li><nuxt-link class="link" to="/">Main</nuxt-link></li>
            <li><nuxt-link class="link" to="/about">About</nuxt-link></li>
            <li><nuxt-link class="link" to="/projects">Projects</nuxt-link></li>
        </ul>
    </nav>
</template>

<style scoped>
.link {
    @apply p-1 hover:bg-gray-200;
}
</style>