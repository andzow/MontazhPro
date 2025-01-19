<script setup lang='ts'>
function start() {
    let vh = window.innerHeight * 0.01;
    document.documentElement.style.setProperty('--vh', `${vh}px`);
}

onMounted(() => {
    start()
})
</script>

<template>
    <section class="main" id="main">
        <div class="main__container">
            <div class="main__position">
                <h1 class="main__title" data-aos="zoom-out-up" data-aos-delay="500">Сварочные, монтажные и электромонтажные услуги</h1>
                <p class="main__text" data-aos="zoom-out-up" data-aos-delay="700">Мы гарантируем высокое качество и безопасность выполнения всех работ в соответствии с действующими стандартами и требованиями. Позвоните и мы оперативно решим все ваши задачи.</p>
                <a class="main__btn" data-aos="zoom-out-up" data-aos-delay="900" href="tel:+79642920280">Позвонить сейчас</a>
            </div>
            <div class="main__image">
                <img class="main__img" src="/Main/main.webp" alt="">
            </div>
            <p class="main__slogan">Ваша проблема - наша задача</p>
        </div>
    </section>
</template>

<style scoped lang="scss">
.main {
    width: 100%;
    height: calc(var(--vh, 1vh) * 100);
    background: var(--darkGreen);
    overflow: hidden;

    &__container {
        max-width: 1800px;
        height: 100%;
        margin: 0 auto;
        padding: 0 20px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        color: var(--white);
        position: relative;
    }

    &__title {
        font-size: 56px;
        max-width: 800px;
        line-height: 56px;
        margin-bottom: 40px;
        font-weight: 800;
        font-family: "Poppins", serif;
    }

    &__text {
        font-size: 20px;
        max-width: 600px;
        margin-bottom: 30px;
    }

    &__image {
        max-width: 800px;
        border-radius: 24px;
        overflow: hidden;
        margin-left: 20px;
    }

    &__img {
        width: 100%;
        object-fit: cover;
    }

    &__btn {
        background: var(--green);
        display: inline-block;
        padding: 15px 35px;
        border-radius: 20px;
        font-size: 20px;
        font-weight: 400;
        transition: all .3s ease;
    }

    &__btn:hover {
        transform: scale(1.03);
    }

    &__slogan {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        bottom: 40px;
        font-size: 18px;
        white-space: nowrap;
    }

    @media(max-width: 1560px) {
        &__title {
            font-size: 48px;
            line-height: 48px;
        }
    }

    @media(max-width: 1500px) {
        &__image {
            max-width: 600px;
        }
    }

    @media(max-width: 1200px) {
        &__image {
            max-width: 500px;
        }
    }

    @media(max-width: 1100px) {
        &__image {
            display: none;
        }

        &__container {
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        &__position {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        &__text,
        &__title {
            text-align: center;
        }
    }

    @media(max-width: 640px) {
        &__title {
            font-size: 35px;
            line-height: 35px;
            margin-bottom: 15px;
        }
    }

    @media(max-width: 340px) {
        &__title {
            font-size: 28px;
            line-height: 28px;
            margin-bottom: 15px;
        }

        &__text {
            font-size: 18px;
        }
    }
}
</style>