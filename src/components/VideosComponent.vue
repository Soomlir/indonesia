<script setup></script>

<template>
  <section class="videos">
    <h2 class="videos__heading">
      Live a life like you wouldn’t imagine, experience a life you wouldn’t
      expect.
    </h2>
    <div class="videos__video">
      <img
        class="videos__bg"
        src="/images/video-bg-1.jpg"
        width="314"
        height="192"
        alt="Обложка видео."
      />
      <button class="videos__play-button videos__play-button--another">
        <span class="visually-hidden">Проиграть видео.</span>
      </button>
    </div>
    <ul class="videos__list">
      <li class="videos__item">
        <div class="video-play">
          <img
            class="videos__bg"
            src="/images/video-bg-2.jpg"
            width="314"
            height="176"
            alt="Обложка видео."
          />
          <button class="video-play__button">
            <span class="visually-hidden">Проиграть видео.</span>
          </button>
        </div>
        <h2 class="videos__title">In The Country</h2>
        <p class="videos__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
          dapibus mauris in lectus tempus.
        </p>
      </li>
      <li class="videos__item">
        <div class="video-play">
          <img
            class="videos__bg videos__bg--another"
            src="/images/video-bg-3.jpg"
            width="314"
            height="176"
            alt="Обложка видео."
          />
          <button class="video-play__button">
            <span class="visually-hidden">Проиграть видео.</span>
          </button>
        </div>
        <h2 class="videos__title">In The City</h2>
        <p class="videos__text">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
          dapibus mauris in.
        </p>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
.videos {
  padding: 86px 30px 2px;
  background-image: url("/images/videos-bg.jpg");
  background-position: 50%;

  @media (min-width: $desktop-width) {
    padding: 154px calc(50% - 720px) 155px;
  }
}

.videos__heading {
  margin: 0;
  margin-bottom: 68px;
  font-size: 40px;
  line-height: 46px;
  text-align: center;
  color: $white-color;

  @media (min-width: $desktop-width) {
    width: 1060px;
    margin-right: auto;
    margin-bottom: 108px;
    margin-left: auto;
  }
}

.videos__list {
  margin: 0;
  padding: 0;
  list-style: none;

  @media (min-width: $desktop-width) {
    display: flex;
    margin-top: 123px;
    margin-left: 110px;

    .videos__bg {
      width: 233px;
      height: 151px;
    }
  }
}

.videos__item {
  margin-bottom: 33px;

  @media (min-width: $desktop-width) {
    display: grid;
    grid-template-columns: 233px 411px;
    grid-template-rows: 40px 180px;
    column-gap: 41px;
  }
}

.videos__title {
  margin: 0;
  margin-bottom: 21px;
  font-size: 22px;
  line-height: 150%;
  text-align: center;
  color: $white-color;

  @media (min-width: $desktop-width) {
    text-align: left;
  }
}

.videos__text {
  margin: 0;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.5px;
  text-align: center;
  color: $white-color;

  @media (min-width: $desktop-width) {
    grid-column: 2/ 3;
    width: 336px;
    text-align: left;
  }
}

.videos__bg {
  position: relative;
  margin-bottom: 40px;
  border-radius: 10px;

  &--another {
    margin-bottom: 31px;
  }

  @media (min-width: $desktop-width) {
    width: 1056px;
    height: 594px;
    margin-bottom: 0;
  }
}

.videos__video {
  position: relative;

  @media (min-width: $desktop-width) {
    width: 1056px;
    height: 594px;
    margin-right: auto;
    margin-bottom: 20px;
    margin-left: auto;
  }
}

.videos__play-button {
  position: absolute;
  inset: 0;
  display: flex;
  width: 67px;
  height: 67px;
  margin: auto;
  background-color: #e93a7d;
  border: none;
  border-radius: 50%;
  cursor: pointer;

  &::before {
    content: "";
    position: absolute;
    inset: 0;
    width: 30px;
    height: 30px;
    margin: auto;
    color: $white-color;
    background-image: url("../icons/play-white.svg");
    background-repeat: no-repeat;
  }

  @media (min-width: $desktop-width) {
    width: 96px;
    height: 96px;

    &--another::before {
      top: 10px;
      left: 13px;
    }
  }
}

.video-play {
  position: relative;
  display: flex;
  height: 151px;
}

.video-play__button {
  position: absolute;
  inset: 0;
  width: 30px;
  height: 30px;
  margin: auto;
  background: transparent;
  background-image: url("../icons/play-white.svg");
  background-repeat: no-repeat;
  background-position: 50%;
  border: none;
  cursor: pointer;
}
</style>
