<script setup>
import DiscoveryComponent from "@/components/DiscoveryComponent.vue";
import HeaderComponent from "@/components/HeaderComponent.vue";
import MapComponent from "@/components/MapComponent.vue";
import PromoComponent from "@/components/PromoComponent.vue";
import StatisticsComponent from "@/components/StatisticsComponent.vue";

import FooterComponent from "./components/FooterComponent.vue";
import GalleryComponent from "./components/GalleryComponent.vue";
import ManualComponent from "./components/ManualComponent.vue";
import VideosComponent from "./components/VideosComponent.vue";
</script>

<template>
	<div class="page">
		<header-component class="page__header" />
		<main>
			<promo-component class="page__promo" />
			<discovery-component class="page__discovery" />
			<statistics-component class="page__statistics" />
			<map-component class="page__map" />
			<videos-component class="page__videos" />
			<gallery-component class="page__gallery" />
			<manual-component class="page__manual" />
		</main>
		<footer-component class="page__footer" />
	</div>
</template>

<!-- <style scoped lang="scss"></style> -->
