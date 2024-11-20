<script setup>
import { ref } from "vue";
import HeadingComponent from "./small/HeadingComponent.vue";
import LinkComponent from "./small/LinkComponent.vue";
import PreviewComponent from "./small/PreviewComponent.vue";

const promoList = ref([
  {
    id: 1,
    title: "Title here",
    text: "Lorem ipsum dolor sit amet et amet ist ame.",
  },
  {
    id: 2,
    title: "Title here",
    text: "Lorem ipsum dolor sit amet et amet ist ame.",
  },
  {
    id: 3,
    title: "Title here",
    text: "Lorem ipsum dolor sit amet et amet ist ame.",
  },
]);
</script>

<template>
  <section class="promo">
    <HeadingComponent class="promo__heading">
      explore indonesia
    </HeadingComponent>
    <LinkComponent class="promo__button">Start travelling</LinkComponent>
    <div class="promo__wrap-list">
      <ol class="promo__list list">
        <li
          class="list__item item"
          v-for="listItem of promoList"
          :key="listItem.id"
        >
          <h2 class="list__title">{{ listItem.title }}</h2>
          <p class="list__text">{{ listItem.text }}</p>
        </li>
      </ol>
      <PreviewComponent />
    </div>
  </section>
</template>

<style scopeed lang="scss">
.page__promo {
  padding: 0 30px;
  padding-bottom: 35px;
}

.promo__heading {
  margin: 0;
  margin-bottom: 9px;
}

.promo__button {
  margin-bottom: 54px;
}

.promo__list {
  margin: 0;
  padding: 0;
  padding: 35px 35px 0 32px;
}

.promo {
  background-image: linear-gradient(
      to top,
      rgba(0, 0, 0, 0.29),
      rgba(0, 0, 0, 0.31)
    ),
    url("../images/header-bg.jpg");
  background-position: 0 -152px;
}

.heading {
  font-size: 58px;
  line-height: 63px;
  font-family: "Roboto", "Arial", sans-serif;
  text-transform: uppercase;
  color: $white-color;
}

.list {
  box-sizing: border-box;
  width: 314px;
  list-style: none;
  background-color: rgba(0, 0, 0, 0.6);
  box-shadow: 0 4px 4px rgba(#000000, 25%);
}

.list__item {
  counter-increment: item;
  margin-bottom: 32px;

  &:last-child {
    margin-bottom: 0;
    padding-bottom: 29px;
  }
}

.list__item::before {
  content: counter(item, decimal-leading-zero);
  font-weight: bold;
  color: $default-red;
}

.list__title {
  margin: 0;
  margin-bottom: 5px;
  font-weight: 700;
  font-size: 26px;
  line-height: 41px;
  color: $white-color;
}

.list__text {
  width: 210px;
  margin: 0;
  font-size: 17px;
  line-height: 24px;
  color: $main-gray;
}
</style>
