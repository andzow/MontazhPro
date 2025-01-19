<script setup lang='ts'>
</script>

<template>
    <section class="about">
        <div class="about__container">
            <div class="about__banner" data-aos="zoom-out-up" data-aos-delay="500">
                <p class="about__name">История нашего успеха</p>
                <h2 class="about__title">От простого проекта до великого достижения</h2>
                <p class="about__text">Когда однажды на заре нашего пути мы столкнулись с задачей монтажа сложной конструкции для большого промышленного объекта, многие сомневались, что мы сможем справиться. Но наша команда верила в успех. Сварочные работы, точные расчеты и электрические системы, которые должны были работать в самых жестких условиях, требовали особого подхода и внимания к деталям. Мы приложили все усилия, чтобы найти оптимальные решения, и результат превзошел все ожидания. Это был наш первый большой проект, и с тех пор мы продолжаем идти по пути совершенствования, предоставляя услуги, которые меняют отрасль и делают мир более безопасным и технологичным.</p>
                <a class="about__btn" href="tel:+79642920280">Свяжитесь с нами!</a>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.about {
    padding-top: 100px;
    background: linear-gradient(to bottom, var(--white) calc(50% + 50px), var(--darkGreen) 50%);
    overflow: hidden;

    &__container {
        max-width: 1800px;
        margin: 0 auto;
        padding: 0 20px;
        position: relative;
    }

    &__banner {
        background: var(--pink);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        border-radius: 25px;
        padding: 60px 30px;
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
        max-width: 1100px;
        margin-bottom: 30px;
        text-align: center;
    }

    &__btn {
        background: #1F2937;
        display: inline-block;
        padding: 15px 35px;
        border-radius: 20px;
        font-size: 20px;
        font-weight: 400;
        transition: all .3s ease;
        color: var(--white);
        cursor: pointer;
    }

    &__btn:hover {
        transform: scale(1.03);
    }

    &__name {
        background: var(--white);
        padding: 5px 10px;
        border-radius: 4px;
        font-size: 20px;
    }

    @media(max-width: 600px) {
        padding-top: 60px;

        &__title {
            font-size: 40px;
            line-height: 40px;
        }

        &__banner {
            padding: 40px 20px;
        }
    }

    @media(max-width: 340px) {
        &__title {
            font-size: 30px;
            line-height: 30px;
            margin-bottom: 20px;
        }

        &__btn {
            padding: 10px 25px;
            font-size: 18px;
        }
    }
}
</style>