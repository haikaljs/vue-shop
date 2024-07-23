<script setup>
import Sidebar from "./Sidebar.vue";
import TopHeader from "./TopHeader.vue";
const { title } = defineProps({
    title: String,
});
</script>

<template>
    <div class="min-h-full flex bg-gray-100">
        <Sidebar />
        <div class="flex-1">
            <TopHeader />
            <main class="p-6">
                <div class="rounded p-4 bg-white">
                    <router-view></router-view>
                </div>
            </main>
        </div>
    </div>
</template>

<style scoped></style>
import TopHeaderVue from "./TopHeader.vue";
