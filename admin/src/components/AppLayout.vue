<script setup>
const { title } = defineProps({
    title: String,
});
</script>

<template>
    <div
        class="flex min-h-full flex-1 flex-col justify-center px-6 py-12 lg:px-8"
    >
        <div class="sm:mx-auto sm:w-full sm:max-w-sm">Part of layout</div>

        <router-view></router-view>
    </div>
</template>

<style scoped></style>
