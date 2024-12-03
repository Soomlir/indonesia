<script setup>
import StatsComponent from "./StatsComponent.vue";
</script>

<template>
	<div class="statistics">
		<section class="explore">
			<h2 class="explore__heading">Explore Our Secrets</h2>
			<div class="explore__slider slider">
				<ul class="slider__list">
					<li class="slider__item slider__item--current">
						<img
							class="slider__img"
							src="/images/slider-img-1.jpg"
							alt="Картинка слайдера 1."
							width="314"
							height="200"
						/>
					</li>
					<li class="slider__item">
						<img
							class="slider__img"
							src="/images/slider-img-2.jpg"
							alt="Картинка слайдера 2."
							width="405"
							height="257"
						/>
					</li>
					<li class="slider__item">
						<img
							class="slider__img"
							src="/images/slider-img-3.jpg"
							alt="Картинка слайдера 3."
							width="405"
							height="257"
						/>
					</li>
				</ul>
				<div class="slider__controls">
					<button class="slider__control" type="radio" name="slide">
						<span class="visually-hidden">Включить слайд 1.</span>
					</button>
					<button class="slider__control" type="radio" name="slide">
						<span class="visually-hidden">Включить слайд 2.</span>
					</button>
					<button class="slider__control" type="radio" name="slide">
						<span class="visually-hidden">Включить слайд 3.</span>
					</button>
					<button
						class="slider__control slider__control--current"
						type="radio"
						name="slide"
					>
						<span class="visually-hidden">Включить слайд 4.</span>
					</button>
					<button class="slider__control" type="radio" name="slide">
						<span class="visually-hidden">Включить слайд 5.</span>
					</button>
				</div>
				<button class="slider__prev">
					<span class="visually-hidden">Предыдущий слайд.</span>
				</button>
				<button class="slider__next">
					<span class="visually-hidden">Следующий слайд.</span>
				</button>
			</div>
		</section>

		<stats-component />
	</div>
</template>

<style lang="scss" scoped>
.statistics {
  background-image: url("/images/explore-bg.jpg");
  background-repeat: no-repeat;

  @media (min-width: 400px) {
    background-image: url("/images/explore-bg-desktop.jpg");
  }
}

.explore {
  position: relative;
  padding: 35px 30px 675px;

  @media (min-width: $desktop-width) {
    padding: 115px calc(50% - 720px) 887px;
  }
}

.explore__heading {
  margin: 0;
  margin-bottom: 33px;
  font-weight: 700;
  font-size: 40px;
  line-height: 46px;
  text-align: center;
  color: $dark-color;

  @media (min-width: $desktop-width) {
    margin-bottom: 34px;
    font-size: 50px;
    line-height: 150%;
  }
}

.slider__list {
  margin: 0;
  padding: 0;
  list-style: none;
  list-style-type: none;

  @media (min-width: $desktop-width) {
    display: flex;
    margin-left: 79px;
  }
}

.slider__item {
  display: none;
  margin-bottom: 3px;

  &--current {
    display: block;
  }

  @media (min-width: $desktop-width) {
    display: block;
    width: 405px;
    height: 257px;
    margin-right: 31px;

    &:nth-child(3) {
      margin-right: 0;
    }

    &--current img {
      width: 100%;
    }
  }
}

.slider__img {
  border-radius: 10px;
}

.slider__controls {
  width: 170px;
  margin-top: 7px;
  margin-right: auto;
  margin-left: auto;

  @media (min-width: $desktop-width) {
    margin-top: 18px;
  }
}

.slider__control {
  width: 17px;
  height: 17px;
  margin: 0;
  margin-right: 14px;
  background-color: $dark-gray;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  appearance: none;

  &:last-child {
    margin-right: 0;
  }

  &--current {
    width: 44px;
    height: 17px;
    background-color: $main-red;
    border-radius: 20px;
  }
}

.slider__prev,
.slider__next {
  position: absolute;
  width: 20px;
  height: 20px;
  background: none;
  background-image: url("../icons/prev-mobile.svg");
  background-repeat: no-repeat;
  background-position: 50%;
  border: none;
  cursor: pointer;

  @media (min-width: $desktop-width) {
    position: absolute;
    width: 40px;
    height: 40px;
    background: none;
    background-image: url("../icons/arrow-slider.svg");
    background-repeat: no-repeat;
    background-position: 50%;
    border: none;
    cursor: pointer;
  }
}

.slider__prev {
  top: 250px;
  left: 3px;

  @media (min-width: $desktop-width) {
    top: 333px;
    left: 12%;
  }
}

.slider__next {
  top: 250px;
  right: 5px;
  transform: rotate(180deg);

  @media (min-width: $desktop-width) {
    top: 333px;
    right: 12%;
  }
}
</style>
