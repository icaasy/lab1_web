<script setup>
const emit = defineEmits(['changePage'])

const services = [
    {
        name: 'Полировка кузова',
        description: 'Удаление мелких царапин, потертостей и следов эксплуатации. Восстанавливает глубину цвета и блеск лакокрасочного покрытия.',
        price: 'от 8 000 ₽',
        time: '4-6 часов'
    },
    {
        name: 'Керамическое покрытие',
        description: 'Защитное покрытие кузова, которое снижает воздействие грязи, воды, ультрафиолета и дорожных реагентов.',
        price: 'от 15 000 ₽',
        time: '4-8 часов'
    },
    {
        name: 'Химчистка салона',
        description: 'Комплексная очистка сидений, ковролина, потолка, пластика и других элементов интерьера автомобиля.',
        price: 'от 7 000 ₽',
        time: '5-8 часов'
    },
    {
        name: 'Защитная пленка',
        description: 'Оклейка элементов кузова прозрачной защитной пленкой для предотвращения сколов, царапин и повреждений.',
        price: 'от 20 000 ₽',
        time: '1-2 дня'
    },
    {
        name: 'Антидождь',
        description: 'Нанесение гидрофобного покрытия на стекла автомобиля для улучшения видимости во время дождя.',
        price: 'от 2 000 ₽',
        time: '1 час'
    },
    {
        name: 'Детейлинг-мойка',
        description: 'Бережная комплексная мойка кузова, колесных дисков, арок и труднодоступных элементов автомобиля.',
        price: 'от 3 000 ₽',
        time: '2-3 часа'
    }
]

function openAuth() {
    emit('changePage', 'auth')
}
</script>

<template>
    <main>
        <section class="catalog-header">
            <div class="container">
                <h1>Услуги детейлинга</h1>

                <p>
                    Выберите подходящую услугу для ухода,
                    восстановления и защиты вашего автомобиля.
                </p>
            </div>
        </section>

        <section class="catalog">
            <div class="container">

                <div class="catalog-grid">
                    <article
                        v-for="service in services"
                        :key="service.name"
                        class="catalog-card"
                    >
                        <h2>{{ service.name }}</h2>

                        <p>{{ service.description }}</p>

                        <div class="service-info">
                            <span>{{ service.price }}</span>
                            <span>{{ service.time }}</span>
                        </div>

                        <button class="button" @click="openAuth">
                            Записаться
                        </button>
                    </article>
                </div>

            </div>
        </section>
    </main>
</template>