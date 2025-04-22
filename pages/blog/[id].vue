<template>
    <div>
        We are in a Blog
    </div>
    <div>
        Post ID: {{ route.params.id }}
    </div>
</template>

<script setup>
    const route = useRoute()

</script>