<script setup>
import { ref } from "vue";
import Sidebar from "./Sidebar.vue";
import TopHeader from "./TopHeader.vue";
const { title } = defineProps({
    title: String,
});

const sidebarOpened = ref(true);

function toggleSidebar() {
    sidebarOpened.value = !sidebarOpened.value;
}
</script>

<template>
    <div class="min-h-full flex bg-gray-100">
        <Sidebar :class="{ '-ml-[200px]': !sidebarOpened }" />
        <div class="flex-1">
            <TopHeader @toggle-sidebar="toggleSidebar" />
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
