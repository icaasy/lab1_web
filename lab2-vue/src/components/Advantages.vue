<script setup>
const advantages = [
    {
        title: 'Качественные материалы',
        text: 'Используем профессиональную автохимию и проверенные средства для ухода за автомобилем.'
    },
    {
        title: 'Опытные мастера',
        text: 'Все работы выполняются специалистами с опытом в сфере автомобильного детейлинга.'
    },
    {
        title: 'Гарантия качества',
        text: 'Контролируем каждый этап работы и отвечаем за качество предоставляемых услуг.'
    }
]
</script>

<template>
    <section class="advantages">
        <div class="container">
            <h2>Почему выбирают AutoDrive?</h2>

            <div class="advantages-grid">
                <div
                    v-for="item in advantages"
                    :key="item.title"
                    class="advantage"
                >
                    <h3>{{ item.title }}</h3>
                    <p>{{ item.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>