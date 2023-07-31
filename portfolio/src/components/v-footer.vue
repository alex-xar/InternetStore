<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__left left">
        <a href="#" class="left__logo"
          ><img
            src="../assets/images/logo.png"
            alt="image"
            class="v-footer__img"
        /></a>
        <div class="left__text">Наш інтернет магазин найкращий на ринку.</div>
        <div class="left__social">
          <a href="https://uk-ua.facebook.com" target="_blank"
            ><img src="../assets/images/7.png" alt="image" /></a
          ><a href="https://www.instagram.com" target="_blank"
            ><img src="../assets/images/8.png" alt="image" /></a
          ><a href="https://twitter.com" target="_blank"
            ><img src="../assets/images/9.png" alt="image"
          /></a>
        </div>
        <a href="#" alt="image" class="left__link">©2023InternetShop</a>
      </div>
      <ul class="right__list">
        <li class="right__item">
          <p class="right__ first">Продукт</p>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Завантажити</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Ціноутворення</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Розташування</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Сервер</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Країни</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Блог</a>
        </li>
      </ul>
      <ul class="right__list">
        <li class="right__item">
          <p class="right__ first">Залучайся</p>
        </li>
        <li class="right__item">
          <a href="" class="right__link">FAQ</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">посібник</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Про нас</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Політика конфіденційності</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Умови використання</a>
        </li>
      </ul>
      <ul class="right__list">
        <li class="right__item">
          <p class="right__ first">Зароблятй гроші</p>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Філіал</a>
        </li>
        <li class="right__item">
          <a href="" class="right__link">Стати партнером</a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "v-footer",
};
</script>

<style lang="scss">
.v-footer {
  &__img {
    width: 100px;
  }
}
.footer {
  margin-top: 100px;
  background: #fae7e7;
  &__absolute {
    position: absolute;
    top: -100%;
  }
  &__container {
    position: relative;
    padding-bottom: 50px;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    gap: 50px;
  }
  &__left {
    width: 340px;
  }
}

.left {
  &__text {
    margin: 30px 0;
  }
  &__social {
    margin-bottom: 30px;
  }
  &__link {
    color: #4f5665;
  }
}
.right {
  &__link {
    line-height: 1.875rem;
    color: #4f5665;
  }
  &__link:hover {
    text-decoration: underline;
  }
}
.first {
  color: #0b132a;
  font-weight: 500;
  font-size: 1.125rem;
  line-height: 1.875rem;
}
</style>
