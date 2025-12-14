<script setup>
import NavbarComponent from "@/components/Header/NavbarComponent.vue";
import SidebarComponent from "@/components/Header/SidebarComponent.vue";
import { ref } from "vue";

const isSidebarOpen = ref(false);

const openSidebar = () => {
  isSidebarOpen.value = true;
};

const closeSidebar = () => {
  isSidebarOpen.value = false;
};
</script>

<template>
  <!-- Navbar -->
  <NavbarComponent @open-sidebar="openSidebar" />

  <!-- Sidebar + Overlay -->
  <Transition name="sidebar">
    <SidebarComponent v-if="isSidebarOpen" @close="closeSidebar" />
  </Transition>
  <!-- Main content -->
  <main class="pt-16">
    <slot />
  </main>
</template>
