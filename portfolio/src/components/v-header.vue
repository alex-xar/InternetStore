<template>
  <header class="v-header">
    <div class="header__container">
      <a href="#" class="header__logo"
        ><img class="v-header__img" src="../assets/images/logo.png" alt="image"
      /></a>
      <nav class="header__menu menu">
        <ul class="menu__list">
          <li class="menu__item">
            <a href="" class="menu__link">Про нас</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">особливості</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">ціноутворення</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">відгуки</a>
          </li>
          <li class="menu__item">
            <a href="" class="menu__link">допомога</a>
          </li>
        </ul>
      </nav>
      <div class="header__button">
        <a href="#" class="header__in">Увійти</a>
        <a href="#" class="header__up animation">Зареєструватися</a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "v-header",
};
</script>

<style lang="scss">
.v-header {
  background-color: #fae7e7;
  &__img {
    width: 100px;
  }
}
.header {
  &__container {
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 10px;
    min-height: 100px;
    padding-top: 10px;
    padding-bottom: 10px;
  }
  &__in {
    margin: 0 30px 0 0;
    color: inherit;
    line-height: 1.1875rem;
    font-weight: 500;
    transition: 1s;
  }
  &__in:hover {
    text-decoration: underline;
  }
  &__up {
    padding: 13px 45px;
    transition: 1s;
  }
}
.menu {
  &__list {
    display: flex;
    column-gap: 40px;
    row-gap: 5px;
    flex-wrap: wrap;
  }
  &__link {
    color: #4f5665;
    line-height: 1.1875rem;
  }
  &__link:hover {
    text-decoration: underline;
  }
}
.animation {
  border: 1px solid red;
  border-radius: 20px;
  color: red;
  font-weight: 500;
}
.animation:hover {
  background-color: red;
  color: #fff;
  transition: 1s;
}

@media (max-width: 990.98px) {
  .header {
    &__container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
      height: 16rem;
    }
  }
}
</style>
