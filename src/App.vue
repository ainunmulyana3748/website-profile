<script setup>
import AppLayout from "./layouts/AppLayout.vue";
import HeroComponent from "./components/HeroComponent.vue";
import ExperienceComponent from "./components/ExperienceComponent.vue";
import PortofolioComponent from "./components/PortofolioComponent.vue";
import ContactComponent from "./components/ContactComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";
</script>

<template>
  <AppLayout>
    <div class="px-15">
      <HeroComponent />
      <ExperienceComponent />
      <PortofolioComponent />
      <ContactComponent />
      <FooterComponent />
    </div>
  </AppLayout>
</template>
