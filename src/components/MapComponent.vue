<script setup></script>

<template>
	<section class="map">
		<h2 class="map__heading">
			Our hills and valleys are like nothing you’ve seen.
		</h2>
		<p class="map__text">
			Lorem ipsum dolor sit amet,
			<br />
			consectetur adipiscing elit. Fusce sit amet magna commodo, tempus dolor
			sit amet, laoreet elit. Donec mauris tortor, elementum sed.
		</p>
		<button class="map__button button">Learn More</button>
	</section>
</template>

<style lang="scss" scoped>
.map {
  padding: 171px 30px 116px;
  background-image: url("/images/map-bg.jpg");

  @media (min-width: 400px) {
    padding: 247px 30px 251px;
    background-image: url("/images/map-bg-desktop.png");
  }

  @media (min-width: $desktop-width) {
    padding: 247px calc(50% - 720px) 210px;
  }
}

.map__heading {
  margin: 0;
  margin-bottom: 37px;
  font-size: 40px;
  line-height: 46px;
  text-align: center;

  @media (min-width: $desktop-width) {
    width: 614px;
    margin-right: auto;
    margin-left: auto;
    font-size: 42px;
    line-height: 50px;
  }
}

.map__text {
  margin: 0;
  margin-bottom: 40px;
  font-size: 17px;
  line-height: 24px;
  text-align: center;
  color: $ligten-gray;

  @media (min-width: $desktop-width) {
    width: 470px;
    margin-right: auto;
    margin-bottom: 40px;
    margin-left: auto;
    font-size: 18px;
    line-height: 28px;
    letter-spacing: 0.5px;

    br {
      display: none;
    }
  }
}

.map__button {
  padding: 23px 46px;
  border-radius: 37px;

  @media (min-width: $desktop-width) {
    width: 210px;
    margin-right: auto;
    margin-left: auto;
  }
}
</style>
