<script setup lang='ts'>
const services = ref([
    {
        type: 'Услуга',
        name: 'Монтажные работы',
        text: "Профессиональная установка конструкций, оборудования и систем любой сложности.",
        image: '/Main/services_1.webp'
    },
    {
        type: 'Услуга',
        name: 'Электромонтажные работы',
        text: "Качественная установка и ремонт электросетей, приборов и оборудования.",
        image: '/Main/services_3.webp'
    },
    {
        type: 'Услуга',
        name: 'Сварочные работы',
        text: "Точность, надежность, долговечность металлоконструкций и соединений.",
        image: '/Main/services_2.webp'
    }
])
</script>

<template>
    <section class="services" id="services">
        <div class="services__container">
            <p class="services__name" data-aos="zoom-out-up" data-aos-delay="500">Услуги</p>
            <h2 class="services__title" data-aos="zoom-out-up" data-aos-delay="500">Сварка и монтаж под ключ</h2>
            <p class="services__text" data-aos="zoom-out-up" data-aos-delay="500">Наши специалисты обладают богатым опытом и профессиональными навыками, что гарантирует надежность, долговечность и эффективность каждого проекта. Мы работаем с индивидуальными заказами любой сложности, обеспечивая быстрое и качественное выполнение задач в срок.</p>
            <div class="services__grid">
                <div class="services__item" v-for="(item, index) in services" :key="index" data-aos="zoom-out-up" data-aos-delay="500">
                    <div>
                        <p class="services__type">{{ item.type }}</p>
                        <h3 class="services__denomination">{{ item.name }}</h3>
                        <p>{{ item.text }}</p>
                    </div>
                    <div class="services__image">
                        <img class="services__img" :src="item.image" alt="">
                    </div>
                    <a class="services__btn" href="tel:+79642920280">Позвонить</a>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.services {
    padding-top: 100px;
    overflow: hidden;

    &__container {
        max-width: 1800px;
        margin: 0 auto;
        padding: 0 20px;
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    &__title {
        font-size: 56px;
        line-height: 56px;
        margin-bottom: 40px;
        font-weight: 800;
        font-family: "Poppins", serif;
        text-align: center;
    }

    &__text {
        font-size: 20px;
        max-width: 900px;
        margin-bottom: 30px;
        text-align: center;
    }

    &__btn {
        background: var(--green);
        display: inline-block;
        padding: 10px 20px;
        border-radius: 20px;
        font-size: 18px;
        font-weight: 400;
        transition: all .3s ease;
        color: var(--white);
        position: relative;
        z-index: 2;
    }

    &__btn:hover {
        transform: scale(1.03);
    }

    &__name {
        background: var(--pink);
        padding: 5px 10px;
        border-radius: 4px;
        font-size: 20px;
    }

    &__grid {
        display: grid;
        max-width: 1500px;
        gap: 30px;
        grid-template-columns: repeat(3, 1fr);
    }

    &__item {
        background: var(--darkGreen);
        color: var(--white);
        border-radius: 15px;
        padding: 30px 20px;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: space-between;
        height: 500px;
        width: 400px;
        position: relative;
        overflow: hidden;
        transition: all .3s ease;
    }

    &__item:hover {
        transform: scale(1.1);
    }

    &__type {
        padding: 5px 8px;
        background: var(--white);
        color: var(--darkGreen);
        border-radius: 10px;
        font-size: 18px;
        font-weight: 600;
        margin-bottom: 15px;
        display: inline-block;
    }

    &__denomination {
        font-size: 24px;
        font-weight: 700;
    }

    &__image {
        width: 300px;
        height: 300px;
        border-radius: 50%;
        overflow: hidden;
        position: absolute;
        z-index: 1;
        bottom: -80px;
        right: -80px;
    }

    &__img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    @media(max-width: 1300px) {
        &__grid {
            gap: 30px;
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media(max-width: 900px) {
        padding-top: 60px;

        &__grid {
            gap: 20px;
            grid-template-columns: repeat(1, 1fr);
        }

        &__item:hover {
            transform: scale(1);
        }
    }

    @media(max-width: 500px) {
        &__item {
            height: 500px;
            width: 100%;
        }

        &__title {
            font-size: 40px;
            line-height: 40px;
        }
    }
}
</style>