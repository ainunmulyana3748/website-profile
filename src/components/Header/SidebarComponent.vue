<template>
  <div
    class="fixed inset-0 z-50 bg-black/40 backdrop-blur-md"
    @click="emit('close')"
  >
    <aside
      class="fixed top-0 left-0 z-60 w-72 min-h-screen bg-base-200 shadow-2xl"
      @click.stop
    >
      <div
        class="h-16 flex justify-between items-center p-4 border-b border-gray-400"
      >
        <span class="text-xl font-bold tracking-widest text-primary">YC</span>
      </div>

      <nav class="flex-1 overflow-y-auto p-3">
        <ul class="space-y-1" v-for="nav in menus">
          <li>
            <a
              :href="nav.href"
              class="flex items-center p-2 text-sm font-medium rounded-lg text-base-content hover:bg-base-300 transition duration-150 active:bg-primary/20"
              @click="emit('close')"
            >
              {{ nav.name }}
            </a>
          </li>
        </ul>
      </nav>
    </aside>
  </div>
</template>

<script setup>
// fungsi closed
const emit = defineEmits(["close"]);

// data array nav for looping
const menus = [
  { name: "Home", href: "#home" },
  { name: "Experience", href: "#experience" },
  { name: "Projects", href: "#projects" },
  { name: "Contact", href: "#contact" },
];
</script>
