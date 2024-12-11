<script setup>
import { ref } from "vue";
const manualList = ref([
  {
    another: false,
    heading: "Bookings your flights",
    id: 1,
    longText: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
					dapibus mauris in lectus tempus, eget tincidunt lacus varius. Sed
					euismod orci dictum faucibus malesuada. Praesent sed eros tincidunt,
					viverra neque auctor, lobortis enim.`,
    text: "Lorem ipsum dolor set,,,,",
    video: false,
  },
  {
    another: true,
    heading: "Choosing your hotel",
    id: 2,
    longText: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
          dapibus mauris in lectus tempus, eget tincidunt lacus varius. Sed
          euismod orci dictum faucibus malesuada. Praesent sed eros tincidunt,
          viverra neque auctor, lobortis enim.`,
    text: "Lorem ipsum dolor set,,,,",
    video: true,
  },
  {
    another: false,
    heading: "Planning your experiences",
    id: 3,
    longText: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
          dapibus mauris in lectus tempus, eget tincidunt lacus varius.`,
    text: "Lorem ipsum dolor set,,,,",
    video: false,
  },
]);
const blockVideo = ref(false);
</script>

<template>
	<section class="manual">
		<h2 class="manual__heading">Getting there</h2>
		<ol class="manual__list">
			<li class="manual__item" v-for="item in manualList" :key="item.id">
				<h3 class="manual__title">{{ item.heading }}</h3>
				<div class="manual__wrap">
					<p class="manual__text">{{ item.text }}</p>
					<a class="manual__link" href="#!">Show more</a>
				</div>
				<p
					class="manual__text-desktop"
					:class="{ 'manual__text-desktop--another': item.another }"
				>
					{{ item.longText }}
				</p>
				<div class="manual__video" v-if="item.video">
					<img
						class="manual__image"
						src="/images/manual-video-1.jpg"
						alt="обложка видео."
					/>
					<button class="manual__play">
						<span class="visually-hidden">Запустить видео.</span>
					</button>
					<div class="manual__video-text" v-if="item.video">
						<h4>Travelling there</h4>
						<p>
							Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus
							dapibus mauris in lectus tempus, eget tincidunt.
						</p>
					</div>
				</div>
				<div class="manual__wrap" v-if="item.video">
					<p class="manual__text">Lorem ipsum dolor set,,,,</p>
					<a class="manual__link" href="#!">Show more</a>
				</div>
			</li>
		</ol>
		<button class="manual__button button">Learn more</button>
	</section>
</template>

<style scoped lang="scss">
.manual {
  padding: 33px 30px 41px;
  background-color: #dce8f2;

  @media (min-width: $desktop-width) {
    padding: 113px calc(50% - 720px) 120px;
  }
}

.manual__heading {
  margin: 0;
  margin-bottom: 41px;
  font-size: 40px;
  line-height: 46px;
  text-align: center;
  color: $dark-color;

  @media (min-width: $desktop-width) {
    margin-bottom: 45px;
    margin-left: 147px;
    font-weight: 700;
    font-size: 60px;
    line-height: 150%;
    text-align: left;
  }
}

.manual__list {
  margin: 0;
  padding: 0;
  list-style: none;

  @media (min-width: $desktop-width) {
    width: 1162px;
    margin-left: 176px;
    border-left: 1px solid $main-gray;
  }
}

.manual__item {
  counter-increment: list;
  position: relative;
  margin-bottom: 32px;
  padding-top: 80px;

  @media (min-width: $desktop-width) {
    margin-bottom: 100px;
    padding: 0;
    padding-left: 67px;

    &:nth-child(3) {
      margin-bottom: 0;
    }
  }
}

.manual__item::before {
  content: counter(list);
  position: absolute;
  top: 0;
  left: 129px;
  display: block;
  box-sizing: border-box;
  width: 56px;
  height: 56px;
  padding-top: 10px;
  font-size: 27px;
  line-height: 38px;
  text-align: center;
  color: $white-color;
  background-color: $default-red;
  border-radius: 50%;

  @media (min-width: $desktop-width) {
    top: -8px;
    left: -29px;
  }
}

.manual__title {
  margin: 0;
  margin-bottom: 7px;
  font-size: 22px;
  line-height: 150%;
  text-align: center;
  color: $dark-color;

  @media (min-width: $desktop-width) {
    font-weight: 700;
    font-size: 27px;
    line-height: 41px;
    text-align: left;
  }
}

.manual__wrap {
  display: contents;

  @media (min-width: $desktop-width) {
    display: none;
  }
}

.manual__text-desktop {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
    width: 1040px;
    margin: 0;
    margin-top: 24px;
    font-size: 24px;
    line-height: 38px;
    color: $main-gray;

    &--another {
      margin-bottom: 105px;
    }
  }
}

.manual__text {
  margin: 0;
  font-size: 17px;
  line-height: 24px;
  text-align: center;
  color: $ligten-gray;
}

.manual__video {
  position: relative;
  margin-top: 32px;
  margin-bottom: 35px;

  @media (min-width: $desktop-width) {
    display: grid;
    grid-template-columns: 250px 450px;
    width: 250px;
    height: 166px;
    column-gap: 45px;

    h4 {
      margin: 0;
      font-weight: 700;
      font-size: 27px;
      line-height: 41px;
      color: $dark-color;
    }

    p {
      margin: 0;
      margin-top: 10px;
      font-size: 22px;
      line-height: 38px;
      color: $ligten-gray;
    }
  }
}

.manual__play {
  position: absolute;
  place-self: center center;
  width: 40px;
  height: 40px;
  background: none;
  background-image: url("../icons/play-white.svg");
  background-repeat: no-repeat;
  background-position: 50%;
  border: none;
  cursor: pointer;
}

.manual__video-text {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
  }
}

.manual__link {
  display: block;
  font-size: 17px;
  line-height: 24px;
  text-decoration: none;
  text-align: center;
  color: $default-red;
}

.manual__button {
  display: none;

  @media (min-width: $desktop-width) {
    display: block;
    width: 210px;
    margin-top: 34px;
    margin-left: 247px;
  }
}
</style>
