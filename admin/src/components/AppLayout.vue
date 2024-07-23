<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import Sidebar from "./Sidebar.vue";
import Navbar from "./Navbar.vue";
const { title } = defineProps({
    title: String,
});

const sidebarOpened = ref(true);

function toggleSidebar() {
    sidebarOpened.value = !sidebarOpened.value;
}

onMounted(() => {
    handleSidebarOpened();
    window.addEventListener("resize", handleSidebarOpened);
});

onUnmounted(() => {
    window.removeEventListener("resize", handleSidebarOpened);
});

function handleSidebarOpened() {
    if (window.outerWidth <= 768) {
        sidebarOpened.value = false;
    } else {
        sidebarOpened.value = true;
    }
    // shorthand
    // sidebarOpened.value = window.outerWidth > 768
}
</script>

<template>
    <div class="min-h-full flex bg-gray-100">
        <Sidebar :class="{ '-ml-[200px]': !sidebarOpened }" />
        <div class="flex-1">
            <Navbar @toggle-sidebar="toggleSidebar" />
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
