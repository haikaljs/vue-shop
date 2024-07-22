<script setup>
import { computed } from "vue";
import store from "./store";

const test = computed(() => store.state.test);
</script>

<template>
    <h1 class="text-3xl font-bold">{{ test }}</h1>
</template>

<style scoped></style>
import { computed } from 'vue';
