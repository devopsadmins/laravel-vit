<template>
    <AppLayout title="Dashboard">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Dashboard
            </h2>
        </template>
        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="bg-white overflow-hidden shadow-xl sm:rounded-lg">
                    <h1 onclick="teste"> Olá {{ nome }}</h1>
                    <ul id="example-1">
                        <li v-for="item in users" :key="item.id">
                            {{ item.name }} - {{ item.email }}
                            <img :src="item.profile_photo_url" style="height: 100px">
                        </li>
                    </ul>
                </div>
            </div>
        </div>

    </AppLayout>
</template>
<script lang="ts" setup>
import AppLayout from '@/Layouts/AppLayout.vue';
import {list} from "postcss";
const nome: string = "Elisangela Lima";
defineProps({
    users: Array
})
</script>
