<script setup>
const emit = defineEmits(['changePage'])

function openCatalog() {
    emit('changePage', 'catalog')
}
</script>

<template>
    <section class="main-section">
        <div class="container main-content">
            <h1>Профессиональный детейлинг вашего автомобиля</h1>

            <p>
                Комплексный уход за автомобилем, восстановление внешнего вида
                и защита кузова с использованием профессиональных материалов.
            </p>

            <button class="button" @click="openCatalog">
                Смотреть услуги
            </button>
        </div>
    </section>
</template>