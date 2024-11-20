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
}

.preview__play {
  position: absolute;
  top: 66px;
  left: 128px;
  width: 59px;
  height: 59px;
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
    top: 12px;
    left: 12px;
    width: 32px;
    height: 32px;
    background-image: var(--icon-play);
  }
}
</style>
