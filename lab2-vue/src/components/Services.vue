<script setup>
const services = [
    {
        name: 'Полировка кузова',
        description: 'Удаление мелких царапин, потертостей и восстановление первоначального блеска лакокрасочного покрытия.'
    },
    {
        name: 'Керамическое покрытие',
        description: 'Защита кузова автомобиля от загрязнений, влаги, ультрафиолета и воздействия окружающей среды.'
    },
    {
        name: 'Химчистка салона',
        description: 'Глубокая очистка сидений, ковролина, пластика и других элементов салона автомобиля.'
    }
]
</script>

<template>
    <section class="services">
        <div class="container">
            <h2>Популярные услуги</h2>

            <div class="services-grid">
                <article
                    v-for="service in services"
                    :key="service.name"
                    class="service-card"
                >
                    <h3>{{ service.name }}</h3>
                    <p>{{ service.description }}</p>
                    <a href="#">Подробнее</a>
                </article>
            </div>
        </div>
    </section>
</template>