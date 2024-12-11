<script setup>
import { ref } from "vue";
const headerLinks = ref([
  { id: 1, text: "destinations" },
  { id: 2, text: "experiences" },
  { id: 3, text: "about" },
  { id: 4, text: "gallery" },
]);
</script>

<template>
  <header class="header">
    <a class="header__logo logo" href="#!">
      <picture>
        <source
          srcset="/images/logo-desktop.svg"
          media="(min-width: 1800px)"
          height="69"
        />
        <img src="/images/logo-mobile.svg" alt="Logo Indonesia." />
      </picture>
    </a>
    <ul class="header__list">
      <li class="header__item" v-for="item in headerLinks" :key="item.id">
        <a class="header__link" href="#!">{{ item.text }}</a>
      </li>
    </ul>
    <div class="header__nav-wrap">
      <a class="header__search search" href="#!">
        <span class="visually-hidden">Открыть поиск.</span>
      </a>
      <a class="header__menu menu" href="#!">
        <span class="visually-hidden">Открыть меню.</span>
      </a>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  padding: 48px 24px;
  padding-right: 28px;
  padding-bottom: 44px;
  background-image: linear-gradient(
      to top,
      rgba(0, 0, 0, 0.29),
      rgba(0, 0, 0, 0.31)
    ),
    url("../images/header-bg.jpg");
  background-repeat: no-repeat;
  background-position: 45% 0;

  @media (min-width: 400px) {
    background-image: linear-gradient(
        to top,
        rgba(0, 0, 0, 0.29),
        rgba(0, 0, 0, 0.31)
      ),
      url("../images/header-bg-desktop.jpg");
    background-position: 0 0;
  }

  @media (min-width: $desktop-width) {
    padding-top: 28px;
    padding-bottom: 62px;
    padding-left: 28px;
    background-image: linear-gradient(
        to top,
        rgba(0, 0, 0, 0.29),
        rgba(0, 0, 0, 0.31)
      ),
      url("../images/header-bg-desktop.jpg");
    background-position: 0 0;
  }
}

.logo {
  display: block;
}

.header__list {
  display: none;

  @media (min-width: $desktop-width) {
    display: flex;
    margin: 0;
    margin-right: auto;
    padding: 0;
    list-style: none;
  }
}

.header__item {
  margin-right: 33px;
}

.header__link {
  display: block;
  padding: 20px 15px;
  font-weight: 700;
  font-size: 18px;
  line-height: 24px;
  text-transform: uppercase;
  text-decoration: none;
  color: $white-color;
}

.search {
  position: relative;
  display: flex;
  width: 24px;
  height: 24px;

  &::before {
    content: "";
    position: absolute;
    inset: 0;
    width: 18px;
    height: 18px;
    margin: auto;
    background-image: url("../icons/search.svg");
  }
}

.menu {
  position: relative;
  display: flex;
  width: 24px;
  height: 24px;

  &::before {
    content: "";
    position: absolute;
    inset: 0;
    width: 18px;
    height: 12px;
    margin: auto;
    background-image: url("../icons/menu.svg");
  }
}

.header__logo {
  margin-right: auto;

  @media (min-width: $desktop-width) {
    margin-right: 48px;
  }
}

.header__search {
  margin-top: 10px;

  @media (min-width: $desktop-width) {
    margin-top: 0;
  }
}

.header__menu {
  margin-top: 8px;
  margin-right: 3px;
  margin-left: 29px;

  @media (min-width: $desktop-width) {
    margin-top: 0;
    margin-left: 40px;
  }
}

.header__nav-wrap {
  display: flex;

  @media (min-width: $desktop-width) {
    margin-right: 109px;
    padding-top: 10px;
  }
}
</style>
