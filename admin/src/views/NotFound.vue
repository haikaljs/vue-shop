<script setup></script>

<template>
    <div
        class="min-h-full flex flex-col items-center justify-center bg-slate-100"
    >
        <div
            class="flex flex-col items-center justify-center p-10 bg-white w-[400px]"
        >
            <h1 class="text-6xl mb-3 font-bold text-zinc-500">404</h1>
            <p class="text-2xl text-zinc-500">Page Not Found</p>
            <router-link
                :to="{ name: 'app.dashboard' }"
                class="px-3 py-1 bg-slate-700 rounded text-white mt-5"
            >
                Go back home
            </router-link>
        </div>
    </div>
</template>

<style scoped></style>
