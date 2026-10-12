<script setup>
defineEmits(['changePage'])
</script>

<template>
    <header class="header">
        <div class="container header-container">
            <a href="#" class="logo" @click.prevent="$emit('changePage', 'home')">
                AutoDrive
            </a>

            <nav class="navigation">
                <a href="#" @click.prevent="$emit('changePage', 'home')">Главная</a>
                <a href="#" @click.prevent="$emit('changePage', 'catalog')">Услуги</a>
                <a href="#" @click.prevent="$emit('changePage', 'about')">О нас</a>
                <a href="#" @click.prevent="$emit('changePage', 'auth')">Войти</a>
            </nav>
        </div>
    </header>
</template>