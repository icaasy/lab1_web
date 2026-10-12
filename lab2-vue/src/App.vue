<script setup>
import { ref, nextTick } from 'vue'

import Header from './components/Header.vue'
import MainSection from './components/MainSection.vue'
import Services from './components/Services.vue'
import Advantages from './components/Advantages.vue'
import About from './components/About.vue'
import Catalog from './components/Catalog.vue'
import Auth from './components/Auth.vue'
import Footer from './components/Footer.vue'

const currentPage = ref('home')

async function changePage(page) {
    if (page === 'about') {
        currentPage.value = 'home'

        await nextTick()

        document.getElementById('about')?.scrollIntoView({
            behavior: 'smooth'
        })

        return
    }

    currentPage.value = page
}
</script>

<template>
    <Header @change-page="changePage" />

    <template v-if="currentPage === 'home'">
        <MainSection @change-page="changePage" />
        <Services @change-page="changePage" />
        <Advantages />
        <About />
    </template>

    <Catalog
        v-else-if="currentPage === 'catalog'"
        @change-page="changePage"
    />

    <Auth v-else-if="currentPage === 'auth'" />

    <Footer />
</template>