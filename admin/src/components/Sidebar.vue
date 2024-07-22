<script setup>
import {
    HomeIcon,
    UsersIcon,
    ViewColumnsIcon,
    ChartBarIcon,
} from "@heroicons/vue/24/solid";
</script>

<template>
    <div class="w-[200px] bg-pink-700 text-white py-4 px-2">
        <router-link
            :to="{ name: 'app.dashboard' }"
            class="flex items-center py-1 px-3 rounded transition-colors hover:bg-black/30 mb-2"
        >
            <span class="mr-2"><HomeIcon class="size-6" /></span>
            <span>Dashboard</span>
        </router-link>
        <router-link
            :to="{ name: 'app.dashboard' }"
            class="flex items-center py-1 px-3 rounded transition-colors hover:bg-black/30 mb-2"
        >
            <span class="mr-2"><ViewColumnsIcon class="size-6" /></span>
            <span>Products</span>
        </router-link>
        <router-link
            :to="{ name: 'app.dashboard' }"
            class="flex items-center py-1 px-3 rounded transition-colors hover:bg-black/30 mb-2"
        >
            <span class="mr-2"><UsersIcon class="size-6" /></span>
            <span>Users</span>
        </router-link>
        <router-link
            :to="{ name: 'app.dashboard' }"
            class="flex items-center py-1 px-3 rounded transition-colors hover:bg-black/30 mb-2"
        >
            <span class="mr-2"><ChartBarIcon class="size-6" /></span>
            <span>Reports</span>
        </router-link>
    </div>
</template>

<style scoped></style>
