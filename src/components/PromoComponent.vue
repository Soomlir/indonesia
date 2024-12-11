<script setup>
import { ref } from "vue";

import HeadingComponent from "./small/HeadingComponent.vue";
import LinkComponent from "./small/LinkComponent.vue";
import PreviewComponent from "./small/PreviewComponent.vue";

const promoList = ref([
  {
    id: 1,
    text: "Lorem ipsum dolor sit amet et amet ist ame.",
    title: "Title here",
  },
  {
    id: 2,
    text: "Lorem ipsum dolor sit amet et amet ist ame.",
    title: "Title here",
  },
  {
    id: 3,
    text: "Lorem ipsum dolor sit amet et amet ist ame.",
    title: "Title here",
  },
]);

const promoSocial = ref([
  { id: 1, text: "Tw" },
  { id: 2, text: "In" },
  { id: 3, text: "Fb" },
]);
</script>

<template>
	<section class="promo">
		<heading-component class="promo__heading">
			explore indonesia
		</heading-component>
		<link-component class="promo__button">Start travelling</link-component>
		<div class="promo__number">
			<span>01</span>
			<div class="promo__progress">
				<div></div>
			</div>
		</div>
		<ul class="promo__social">
			<li v-for="item in promoSocial" :key="item.id">{{ item.text }}</li>
		</ul>
		<div class="promo__wrap-list">
			<ol class="promo__list promo-list">
				<li
					class="promo-list__item"
					v-for="listItem of promoList"
					:key="listItem.id"
				>
					<h2 class="promo-list__title">{{ listItem.title }}</h2>
					<p class="promo-list__text">{{ listItem.text }}</p>
				</li>
			</ol>
			<preview-component />
		</div>
	</section>
</template>

<style scopeed lang="scss">
.page__promo {
  padding: 0 30px;
  padding-bottom: 40px;

  @media (min-width: $desktop-width) {
    padding: 106px 0 0 277px;
  }
}

.promo__heading {
  margin: 0;
  margin-bottom: 9px;

  @media (min-width: $desktop-width) {
    width: 700px;
    margin-bottom: 22px;
    font-size: 120px;
    line-height: 130px;
  }
}

.promo__button {
  margin-bottom: 54px;

  @media (min-width: $desktop-width) {
    width: 272px;
    margin-bottom: 0;
    padding: 26px 40px;
    font-size: 20px;
    border-radius: 40px;
  }
}

.promo {
  background-image: linear-gradient(
      to top,
      rgba(0, 0, 0, 0.29),
      rgba(0, 0, 0, 0.31)
    ),
    url("../images/header-bg.jpg");
  background-repeat: no-repeat;
  background-position: 45% -152px;

  @media (min-width: 400px) {
    background-image: linear-gradient(
        to top,
        rgba(0, 0, 0, 0.29),
        rgba(0, 0, 0, 0.31)
      ),
      url("../images/header-bg-desktop.jpg");
    background-position: 0 -159px;
  }

  @media (min-width: $desktop-width) {
    position: relative;
    background-image: linear-gradient(
        to top,
        rgba(0, 0, 0, 0.29),
        rgba(0, 0, 0, 0.31)
      ),
      url("../images/header-bg-desktop.jpg");
    background-position: 0 -159px;
  }
}

.heading {
  font-size: 58px;
  line-height: 63px;
  font-family: "Roboto", "Arial", sans-serif;
  text-transform: uppercase;
  color: $white-color;
}

.promo__number {
  display: none;

  @media (min-width: $desktop-width) {
    position: absolute;
    top: 277px;
    left: -148px;
    display: flex;
    align-items: center;
    width: 440px;
    transform: rotate(-90deg);

    span {
      display: block;
      margin-right: 20px;
      font-weight: 700;
      font-size: 16px;
      line-height: 24px;
      color: $white-color;
    }
  }
}

.promo__progress {
  position: relative;
  display: flex;
  width: 398px;
  height: 2px;
  background-color: $white-color;

  &::after {
    content: "";
    position: absolute;
    top: -1px;
    right: 0;
    width: 100px;
    height: 4px;
    background-color: $default-red;
  }
}

.promo__social {
  display: none;

  @media (min-width: $desktop-width) {
    position: absolute;
    top: 77%;
    left: 60px;
    display: block;
    margin: 0;
    padding: 0;
    list-style: none;
    font-weight: 700;
    font-size: 16px;
    line-height: 24px;
    color: $white-color;

    li {
      width: 30px;
      margin-top: 30px;
      transform: rotate(-90deg);

      &:last-child {
        margin-right: 0;
      }
    }
  }
}

.promo__wrap-list {
  @media (min-width: $desktop-width) {
    display: flex;
    margin-top: 197px;
  }
}

.promo-list {
  box-sizing: border-box;
  width: 314px;
  margin: 0;
  padding: 0;
  padding: 35px 35px 0 32px;
  list-style: none;
  background-color: rgba(0, 0, 0, 0.6);
  box-shadow: 0 4px 4px rgba(#000000, 25%);

  @media (min-width: $desktop-width) {
    display: flex;
    display: grid;
    align-self: flex-end;
    grid-template-columns: 1fr 1fr 1fr;
    width: 1227px;
    min-height: 210px;
    padding-right: 0;
    column-gap: 32px;
  }
}

.promo-list__item {
  counter-increment: item;
  margin-bottom: 32px;

  &:last-child {
    margin-bottom: 0;
    padding-bottom: 29px;
  }

  @media (min-width: $desktop-width) {
    margin-bottom: 0;
    padding: 5px 39px;
  }
}

.promo-list__item::before {
  content: counter(item, decimal-leading-zero);
  font-weight: bold;
  color: $default-red;
}

.promo-list__title {
  margin: 0;
  margin-bottom: 5px;
  font-weight: 700;
  font-size: 26px;
  line-height: 41px;
  color: $white-color;
  @media (min-width: $desktop-width) {
    margin-top: 12px;
  }
}

.promo-list__text {
  width: 210px;
  margin: 0;
  font-size: 17px;
  line-height: 24px;
  color: $main-gray;

  @media (min-width: $desktop-width) {
    font-size: 19px;
  }
}

.promo__preview img {
  @media (min-width: $desktop-width) {
    width: 418px;
    height: 254px;
  }
}
</style>
