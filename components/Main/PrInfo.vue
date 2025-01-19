<script setup lang='ts'>
const infoArray = ref([
    {
        name: "Монтажные работы: создание надежных и безопасных конструкций",
        text: "Монтажные работы включают в себя установку различных конструкций и систем, таких как металлоконструкции, вентиляция, отопление, а также монтаж крыш и фасадов. Применение качественных монтажных технологий напрямую влияет на срок службы зданий и сооружений.",
        image: "/Main/info_1.webp"
    },
    {
        name: "Электромонтажные работы: безопасность и эффективность электрических систем",
        text: "Электромонтажные работы включают в себя установку, прокладку и подключение всех видов электрических систем, от распределительных щитов до световых и отопительных систем. Важно, чтобы электромонтажные работы выполнялись квалифицированными специалистами, так как ошибки на этом этапе могут привести к коротким замыканиям, перегрузке электрических систем и даже пожарам.",
        image: "/Main/info_2.webp"
    },
])
</script>

<template>
    <section class="info">
        <div class="info__container">
            <div class="info__item" :class="{'info__item_reverse': idx % 2 === 0}" v-for="(item, idx) in infoArray" :key="idx" data-aos="zoom-out-up" data-aos-delay="500">
                <div class="info__image">
                    <img :src="item.image" alt="">
                </div>
                <div class="info__position" :class="{'info__position_reverse': idx % 2 === 0}">   
                    <h3 class="info__title">{{ item.name }}</h3>
                    <p class="info__text">{{ item.text }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.info {
    padding-top: 100px;
    overflow: hidden;

    &__container {
        max-width: 1600px;
        margin: 0 auto;
        padding: 0 20px;
        position: relative;
    }

    &__item {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &__item_reverse {
        flex-direction: row-reverse;
    }
    
    &__position {
        max-width: 800px;
        margin-left: 20px;
    }

    &__position_reverse {
        margin-left: 0px;
        margin-right: 20px;
    }

    &__image {
        border-radius: 24px;
        overflow: hidden;
    }

    &__title {
        font-size: 56px;
        line-height: 56px;
        margin-bottom: 40px;
        font-weight: 800;
    }

    &__text {
        font-size: 20px;
        max-width: 900px;
        margin-bottom: 30px;
    }

    @media(max-width: 1300px) {
        &__position {
            max-width: 700px;
        }
    }

    @media(max-width: 1200px) {
        &__title {
            font-size: 46px;
            line-height: 46px;
        }

        &__position {
            max-width: 600px;
        }
    }

    @media(max-width: 1100px) {
        &__position {
            max-width: 500px;
        }
    }

    @media(max-width: 900px) {
        padding-top: 60px;

        &__item {
            flex-direction: column-reverse;
            margin-bottom: 20px;
        }

        &__position {
            margin-left: 0px;
            margin-right: 0px;
        }
    }

    @media(max-width: 600px) {
        &__title {
            font-size: 26px;
            line-height: 26px;
            margin-bottom: 20px;
        }
    }

    @media(max-width: 340px) {
        &__title {
            font-size: 30px;
            line-height: 30px;
            margin-bottom: 20px;
        }
    }
}
</style>