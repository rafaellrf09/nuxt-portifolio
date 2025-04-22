<template>
    <div class="container mx-auto max-w-2xl">
        <header class="flex justify-between items-center mt-5">
            <div>
                <nuxt-link to="/" class="text-xl font-semibold p-2 hover:bg-gray-200">Rafael Figueiredo</nuxt-link>
            </div>
            <nav class="font-mono">
                <ul class="flex space-x-4">
                    <li><nuxt-link to="/">Main</nuxt-link></li>
                    <li><nuxt-link to="/about">About</nuxt-link></li>
                    <li><nuxt-link to="/blog">Blog</nuxt-link></li>
                </ul>
            </nav>
        </header>

        <main class="p-2">
            <slot />
        </main>
    </div>
</template>