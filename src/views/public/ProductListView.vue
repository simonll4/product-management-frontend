<script setup lang="ts">
import Footer from '@/components/navigation/Footer.vue';
import NavBar from '@/components/NavBar.vue';
import SideBar from '@/components/SideBar.vue';
import ProductList from '@/components/product/ProductList.vue';
import { computed } from 'vue';

const isAuthenticated = computed(() => localStorage.getItem('token'));
</script>

<template>
    <v-app>
        <v-layout class="d-flex flex-column min-vh-100">
            <NavBar />
            <v-col class="d-flex">
                <SideBar v-if="isAuthenticated" />
                <v-main class="d-flex flex-column flex-grow-1">
                    <ProductList />
                </v-main>
            </v-col>
        </v-layout>
    </v-app>
    <Footer />
</template>

<style scoped>
.nav-title {
    font-weight: 700;
    padding: 10px;
}

.v-container {
    border: 0.1px solid #dee2e6;
    border-radius: 4px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.min-vh-100 {
    min-height: 100vh;
}

.flex-grow-1 {
    flex-grow: 1;
}
</style>