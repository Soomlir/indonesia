<script setup>
import { ref } from "vue";
const discoveryList = ref([
  {
    heading: "The walkways of Indonesia spellbind",
    id: 1,
    img: {
      alt: "Прекрасный вид 1.",
      height: 232,
      src: "images/view-1.png",
      width: 314,
    },
    text: `Lorem ipsum dolor sit amet, conse
            <br class="mobile" />
            ctetur adip
            <br class="desktop" />
            iscing elit. Fusce commodo magna et libero
            <br class="desktop" />
            mollis rhoncus.`,
  },
  {
    heading: "Perfect beaches exude relaxation and fun",
    id: 2,
    img: {
      alt: "Прекрасный вид 2.",
      height: 224,
      src: "images/view-2.png",
      width: 314,
    },
    text: `Lorem ipsum dolor sit amet, conse ctetur adip iscing elit. Fusce
        commodo magna et libero mollis rhoncus.`,
  },
]);
</script>

<template>
  <section class="discovery">
    <h2 class="visually-hidden">Discovery</h2>
    <ul class="discovery__list">
      <li
        v-for="{ id, img, heading, text } in discoveryList"
        :key="id"
        class="discovery__item"
      >
        <img
          class="discovery__img"
          :src="img.src"
          :width="img.width"
          :height="img.height"
          :alt="img.alt"
        />
        <div class="discovery__wrap">
          <h3 class="discovery__heading">
            {{ heading }}
          </h3>
          <p class="discovery__text" v-html="text"></p>
          <a href="#!" class="discovery__button button">Learn more</a>
        </div>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
.discovery {
  padding: 0 30px;
  padding-top: 40px;
  padding-bottom: 49px;
  background-image: url("/images/discovery-bg.jpg");
  background-repeat: no-repeat;
  background-position: 77% 50%;

  @media (min-width: $desktop-width) {
    padding: 207px calc(50% - 720px) 263px;
  }
}

.discovery__list {
  max-width: 1800px;
  margin: 0;
  padding: 0;
  list-style: none;

  @media (min-width: $desktop-width) {
    margin-left: 101px;
  }
}

.discovery__wrap {
  @media (min-width: $desktop-width) {
    width: 480px;
    padding-top: 61px;

    &--another {
      margin-left: 0;
      padding: 0;
      padding-top: 67px;
    }
  }
}

.discovery__item {
  margin-bottom: 57px;

  &:last-child {
    margin-bottom: 0;
  }

  @media (min-width: $desktop-width) {
    display: flex;
    gap: 131px;
    margin-bottom: 163px;

    &:last-child {
      margin-bottom: 0;
      padding-left: 38px;
    }

    &:last-child img {
      order: 1;
    }
  }
}

.discovery__img {
  margin-bottom: 29px;
  border-radius: 10px;

  &--another {
    margin-bottom: 42px;
  }

  @media (min-width: $desktop-width) {
    width: 631px;
    height: 460px;
  }
}

.discovery__heading {
  width: 310px;
  margin: 0;
  margin-bottom: 20px;
  font-size: 40px;
  line-height: 46px;
  color: $white-color;

  &--another {
    margin-bottom: 27px;
  }

  @media (min-width: $desktop-width) {
    width: auto;
    font-weight: 700;
    font-size: 42px;
    line-height: 50px;
    text-shadow: 0 4px 4px rgba(#000000, 25%);
  }
}

.discovery__text {
  margin: 0;
  margin-bottom: 35px;
  font-size: 17px;
  line-height: 24px;
  color: $light-gray;

  .desktop {
    display: none;
  }

  &--another {
    margin-bottom: 20px;
  }

  @media (min-width: $desktop-width) {
    margin-bottom: 33px;
    font-size: 18px;
    line-height: 28px;
    letter-spacing: 1%;

    .mobile {
      display: none;
    }

    .desktop {
      display: block;
    }

    &--another {
      margin-bottom: 59px;
    }
  }
}

.discovery__button {
  padding: 22px 32px;

  @media (min-width: $desktop-width) {
    width: 180px;
    padding: 15px 20px;
  }
}
</style>
