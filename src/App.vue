<script setup>
import HeaderComponent from "@/components/HeaderComponent.vue";
import PromoComponent from "@/components/PromoComponent.vue";
import DiscoveryComponent from "@/components/DiscoveryComponent.vue";
import ExploreComponent from "@/components/ExploreComponent.vue";
import StatsComponent from "@/components/StatsComponent.vue";
</script>

<template>
  <div class="page">
    <header-component class="page__header" />
    <main>
      <PromoComponent class="page__promo" />
      <DiscoveryComponent class="page__discovery" />
      <ExploreComponent class="page__explore" />
      <StatsComponent class="page__stats" />
    </main>
    <footer>footer</footer>
  </div>
</template>

<!-- <style scoped lang="scss"></style> -->
