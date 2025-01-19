<script setup lang='ts'>
</script>

<template>
    <section class="about" id="about">
        <div class="about__container">
            <div class="about__banner" data-aos="zoom-out-up" data-aos-delay="500">
                <p class="about__name">О компании</p>
                <h2 class="about__title">Мы единое целое</h2>
                <p class="about__text">Компания, предоставляющая сварочные, монтажные и электромонтажные услуги. Мы предлагаем высококачественные решения для различных строительных и промышленных проектов. Наша команда профессионалов выполняет работы с использованием современного оборудования, обеспечивая надежность и безопасность на каждом этапе.</p>
                <a class="about__btn" href="tel:+79642920280">Появились вопросы?</a>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.about {
    padding-top: 100px;
    background: linear-gradient(to bottom, var(--darkGreen) calc(50% + 50px), var(--white) 50%);
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
        max-width: 900px;
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
            font-size: 46px;
            line-height: 46px;
        }

        &__banner {
            padding: 40px 20px;
        }
    }
}
</style>