<script setup>
import { ref } from "vue";

const imagesList = ref([
  {
    alt: "",
    className: "images__image--1",
    height: 217,
    id: 1,
    src: "images/gallery-1.jpg",
    width: 151,
  },
  {
    alt: "",
    className: "images__image--2",
    height: 86,
    id: 2,
    src: "images/gallery-2.jpg",
    width: 151,
  },
  {
    alt: "",
    className: "images__image--3",
    height: 86,
    id: 3,
    src: "images/gallery-3.jpg",
    width: 151,
  },
  {
    alt: "",
    className: "images__image--4",
    height: 217,
    id: 4,
    src: "images/gallery-4.jpg",
    width: 151,
  },
  {
    alt: "",
    className: "images__image--5",
    height: 153,
    id: 5,
    src: "images/gallery-5.jpg",
    width: 150,
  },
  {
    alt: "",
    className: "images__image--6",
    height: 153,
    id: 5,
    src: "images/gallery-6.jpg",
    width: 150,
  },
]);
</script>

<template>
	<section class="gallery">
		<h2 class="gallery__heading">Photo Gallery</h2>
		<p class="gallery__text">
			Lorem ipsum dolor sit amet,
			<br />
			consectetur adipiscing elit. Phasellus dapibus mauris in lectus tempus,
			eget tincidunt.
		</p>
		<div class="gallery__images images">
			<a href="#!" v-for="element in imagesList" :key="element.id">
				<img
					:class="element.className"
					:src="element.src"
					:width="element.width"
					:height="element.height"
					:alt="element.alt"
				/>
			</a>
		</div>
	</section>
</template>

<style lang="scss" scoped>
.gallery {
  padding: 35px 30px 40px;

  @media (min-width: $desktop-width) {
    padding: 158px calc(50% - 720px) 230px;
  }
}

.gallery__heading {
  margin: 0;
  margin-bottom: 22px;
  font-size: 40px;
  line-height: 46px;
  text-align: center;
  color: $dark-color;

  @media (min-width: $desktop-width) {
    font-weight: 700;
    font-size: 60px;
    line-height: 150%;
  }
}

.gallery__text {
  margin: 0;
  margin-bottom: 33px;
  font-size: 17px;
  line-height: 24px;
  text-align: center;
  color: $ligten-gray;

  @media (min-width: $desktop-width) {
    width: 500px;
    margin-right: auto;
    margin-bottom: 61px;
    margin-left: auto;
    font-size: 18px;
    line-height: 28px;
    letter-spacing: 1%;

    br {
      display: none;
    }
  }
}

.gallery__images {
  display: grid;
  gap: 12px 13px;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 86px 118px;

  a {
    display: contents;
  }

  @media (min-width: $desktop-width) {
    gap: 30px;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 210px 130px 130px 210px;
    width: 1170px;
    margin-right: auto;
    margin-left: auto;
  }
}

.images__image--1 {
  grid-row: 1 /3;

  @media (min-width: $desktop-width) {
    width: 370px;
    height: 530px;
  }
}

.images__image--2 {
  @media (min-width: $desktop-width) {
    width: 370px;
    height: 210px;
  }
}

.images__image--3 {
  @media (min-width: $desktop-width) {
    grid-row: 4 / 5;
    width: 370px;
    height: 210px;
  }
}

.images__image--4 {
  grid-column: 2 / -1;
  grid-row: 2 / 4;

  @media (min-width: $desktop-width) {
    width: 370px;
    height: 530px;
  }
}

.images__image--5 {
  @media (min-width: $desktop-width) {
    grid-column: 3 / 4;
    grid-row: 1 /2;
    width: 370px;
    height: 370px;
  }
}

.images__image--6 {
  @media (min-width: $desktop-width) {
    grid-column: 3 / 4;
    grid-row: 3 /5;
    width: 370px;
    height: 370px;
  }
}
</style>
