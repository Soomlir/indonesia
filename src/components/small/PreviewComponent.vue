<script setup></script>

<template>
  <div class="promo__preview preview">
    <img src="/images/video-preview-bg.jpg" alt="Фон видео." />
    <button class="preview__play">
      <span class="visually-hidden">Проиграть видео.</span>
    </button>
  </div>
</template>

<style lang="scss" scoped>
.preview {
  position: relative;
  display: flex;
}

.preview__play {
  position: absolute;
  inset: 0;
  width: 59px;
  height: 59px;
  margin: auto;
  background: none;
  background-color: #ffffff;
  background-repeat: no-repeat;
  border: none;
  border-radius: 50%;
  box-shadow: 0 0 50px rgba(#000000, 50%);
  cursor: pointer;

  &::before {
    content: "";
    position: absolute;
    inset: 0;
    width: 32px;
    height: 32px;
    margin: auto;
    background-image: var(--icon-play);
  }

  @media (min-width: 1920px) {
    width: 79px;
    height: 79px;
  }
}
</style>
