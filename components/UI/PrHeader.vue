<script setup>
const route = useRoute();
const router = useRouter();
function scrollToTop () {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
    })
}

function scrollToAnchor(anchorMain) {
  if (route.name === "index") {
    const anchor = document.getElementById(anchorMain);
    if (anchor) {
      const offset = 90;
      const top = anchor.getBoundingClientRect().top + window.scrollY - offset;
      window.scrollTo({ top, behavior: 'smooth' });
    }
  } else {
    const newRoute = { path: '/', hash: `#${anchorMain}`};
    router.push(newRoute);
  }
}
</script>


<template>
  <header class="header">
    <div class="header__container">
      <h2 class="header__logo">Монтаж<span class="header__span">Про</span></h2>
      <nav>
        <ul class="header__nav">
          <li @click="scrollToAnchor('main')" class="header__item">Главная</li>
          <li @click="scrollToAnchor('about')" class="header__item">Компания</li>
          <li @click="scrollToAnchor('services')" class="header__item">Услуги</li>
          <li @click="scrollToAnchor('gallery')" class="header__item">ФотоГалерея</li>
        </ul>
      </nav>
      <a class="header__btn" href="tel:+79642920280">Позвонить</a>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  position: fixed;
  padding: 30px 0;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 50;
  background: var(--darkGreen);
    overflow: hidden;


  &__container {
  padding: 0 20px;
  margin: 0 auto;
  max-width: 1800px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  color: var(--white);
}

&__nav {
  display: flex;
  align-items: center;
  color: var(--white);
}

&__item {
  cursor: pointer;
  padding-bottom: 3px;
  font-size: 20px;
  transition: all .3s ease;
  position: relative;
  font-weight: 500;
}

&__item:hover {
  color: var(--green);
  transform: translateY(-3px);
}

&__item:not(:last-child) {
  margin-right: 30px;
}

&__item:after {
  content: "";
  display: block;
  position: absolute;
  right: 0;
  bottom: -3px;
  width: 0;
  height: 2px;
  background-color: var(--green);
  transition: width 0.5s;
}

&__item:hover:after {
  content: "";
  width: 100%;
  display: block;
  position: absolute;
  left: 0;
  bottom: -3px;
  height: 2px;
  background-color: var(--green);
  transition: width 0.5s;
  font-weight: 500;
}

&__logo {
  color: var(--white);
  font-weight: 700;
  font-size: 22px;
}

&__span {
  color: var(--green);
  font-weight: 900;
}

&__btn {
    background: var(--green);
    display: inline-block;
    padding: 10px 30px;
    border-radius: 20px;
    font-size: 18px;
    font-weight: 400;
    transition: all .3s ease;
}

&__btn:hover {
    transform: scale(1.03);
}

@media(max-width: 800px) {
  &__nav {
    display: none;
  }
}
}

</style>