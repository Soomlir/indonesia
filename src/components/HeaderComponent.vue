<script setup></script>

<template>
  <header class="header">
    <a class="header__logo logo" href="#!">
      <img src="/images/logo-mobile.svg" alt="Logo Indonesia." />
    </a>
    <a class="header__search search" href="#!">
      <span class="visually-hidden">Открыть поиск.</span>
    </a>
    <a class="header__menu menu" href="#!">
      <span class="visually-hidden">Открыть меню.</span>
    </a>
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
}

.logo {
  display: block;
  width: 149px;
  height: 60px;
}

.search {
  position: relative;
  display: block;
  width: 24px;
  height: 24px;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 18px;
    height: 18px;
    background-image: url("../icons/search.svg");
  }
}

.menu {
  position: relative;
  display: block;
  width: 24px;
  height: 24px;

  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 18px;
    height: 12px;
    background-image: url("../icons/menu.svg");
  }
}

.header__logo {
  margin-right: auto;
}

.header__search {
  margin-top: 13px;
}

.header__menu {
  margin-top: 14px;
  margin-left: 29px;
}
</style>
