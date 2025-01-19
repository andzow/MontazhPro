<script setup lang='ts'>
</script>

<template>
    <section class="gallery" id="gallery">
        <div class="gallery__container">
            <p class="gallery__name" data-aos="zoom-out-up" data-aos-delay="500">ФотоГалерея</p>
            <h2 class="gallery__title" data-aos="zoom-out-up" data-aos-delay="500">Взгляд на нашу работу</h2>
            <p class="gallery__text" data-aos="zoom-out-up" data-aos-delay="500">Каждое наше фото — это история о том, как мы решаем задачи с точностью и мастерством. В этой галерее вы увидите результаты нашей работы: сварочные, монтажные и электромонтажные проекты, выполненные с максимальным вниманием к деталям. Мы уверены, что наш опыт и профессионализм ярко отражаются в каждом кадре. Просмотрите нашу галерею и убедитесь сами, как высоко мы ценим качество и надежность в каждом проекте.</p>
            <div class="gallery__grid">
                <img class="gallery__img gallery__1" src="/Main/gallery_1.webp" alt="" data-aos="zoom-out-up" data-aos-delay="500">
                <img class="gallery__img gallery__2" src="/Main/gallery_2.webp" alt="" data-aos="zoom-out-up" data-aos-delay="500">
                <img class="gallery__img gallery__3" src="/Main/gallery_3.webp" alt="" data-aos="zoom-out-up" data-aos-delay="500">
                <img class="gallery__img gallery__4" src="/Main/gallery_4.webp" alt="" data-aos="zoom-out-up" data-aos-delay="500">
                <img class="gallery__img gallery__5" src="/Main/gallery_5.webp" alt="" data-aos="zoom-out-up" data-aos-delay="500">
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.gallery {
    padding-top: 100px;
    background: var(--darkGreen);
    overflow: hidden;

    &__container {
        max-width: 1800px;
        margin: 0 auto;
        padding: 0 20px;
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
        color: var(--white);
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

    &__name {
        background: var(--pink);
        padding: 5px 10px;
        border-radius: 4px;
        font-size: 20px;
        color: var(--black);
    }

    &__img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        border-radius: 24px;
    }

    &__1 {
        grid-area: gallery_1;
    }
    &__2 {
        grid-area: gallery_2;
    }
    &__3 {
        grid-area: gallery_3;
    }
    &__4 {
        grid-area: gallery_4;
    }
    &__5 {
        grid-area: gallery_5;
    }

    &__grid {
        display: grid;
        max-width: 1200px;
        gap: 25px;
        grid-template-areas:
        "gallery_1 gallery_3 gallery_5"
        "gallery_1 gallery_3 gallery_5"
        "gallery_1 gallery_4 gallery_5"
        "gallery_2 gallery_4 gallery_5";
        grid-template-columns: repeat(3, 1fr);
    }

    @media(max-width: 600px) {
        padding-top: 60px;

        &__title {
            font-size: 40px;
            line-height: 40px;
        }

        &__grid {
            grid-template-areas:
            "gallery_1"
            "gallery_2"
            "gallery_3"
            "gallery_4"
            "gallery_5"
            "gallery_6";
            grid-template-columns: repeat(1, 1fr);
        }
    }

    @media(max-width: 500px) {
        &__title {
            font-size: 40px;
            line-height: 40px;
        }
    }
}
</style>