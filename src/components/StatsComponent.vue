<script setup></script>

<template>
  <section class="stats">
    <h2 class="stats__heading">By The Numbers</h2>
    <p class="stats__text">
      Lorem ipsum dolor sit amet,
      <br />
      consectetur adipiscing elit. Fusce commodo magna et libero.Lorem ipsum
      dolor sit amet, consectetur adipiscing elit.
    </p>
    <ul class="stats__list">
      <li class="stats__item">
        <p class="stats__number">100+</p>
        <p class="stats__text-list">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo
          magna et libero.
        </p>
      </li>
      <li class="stats__item">
        <p class="stats__number">43,000+</p>
        <p class="stats__text-list">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce
          commodo.
        </p>
      </li>
      <li class="stats__item">
        <p class="stats__number">30+</p>
        <p class="stats__text-list">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce commodo
          magna et libero.
        </p>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
.stats {
  padding: 52px 30px 68px;
  background-color: rgba($darken-color, 90%);

  @media (min-width: $desktop-width) {
    padding: 206px calc(50% - 720px) 179px;
  }
}

.stats__heading {
  margin: 0;
  margin-bottom: 37px;
  font-weight: 700;
  font-size: 40px;
  line-height: 46px;
  text-align: center;
  color: $white-color;

  @media (min-width: $desktop-width) {
    font-size: 60px;
  }
}

.stats__text {
  margin: 0;
  margin-bottom: 62px;
  font-size: 17px;
  line-height: 24px;
  text-align: center;
  color: $light-gray;

  @media (min-width: $desktop-width) {
    width: 500px;
    margin-right: auto;
    margin-left: auto;
    font-size: 18px;
    line-height: 28px;
    letter-spacing: 0.5px;

    br {
      display: none;
    }
  }
}

.stats__list {
  margin: 0;
  padding: 0;

  @media (min-width: $desktop-width) {
    display: flex;
    justify-content: space-between;
  }
}

.stats__item {
  margin-bottom: 80px;

  &:nth-child(2) {
    margin-bottom: 43px;
  }

  &:last-child {
    margin-bottom: 0;
  }

  @media (min-width: $desktop-width) {
    width: 380px;
  }
}

.stats__number {
  margin: 0;
  margin-bottom: 7px;
  font-weight: 700;
  font-size: 40px;
  line-height: 46px;
  text-align: center;
  color: $main-red;
}

.stats__text-list {
  margin: 0;
  font-size: 17px;
  line-height: 24px;
  text-align: center;
  color: $light-gray;
}
</style>
