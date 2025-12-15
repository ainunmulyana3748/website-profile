<script setup>
import profileImg from "../assets/img/Profile.png";

const techs = [
  "React",
  "Next.js",
  "Vue",
  "Laravel",
  "Javascript",
  "TypeScript",
  "PHP",
  "Tailwind",
];
</script>

<template>
  <main class="relative min-h-screen overflow-hidden pt-16" id="home">
    <section class="relative flex min-h-screen justify-center">
      <!-- Main content -->
      <div class="relative z-10 text-center">
        <!-- Profile image -->
        <div class="relative mx-auto mb-2 inline-block">
          <img :src="profileImg" alt="Profile" class="w-[350px] object-cover" />
        </div>

        <!-- Typography -->
        <div>
          <div class="space-y-2">
            <h1
              class="text-pretty text-7xl font-bold leading-none tracking-tight text-foreground sm:text-8xl lg:text-9xl"
            >
              Fullstack
            </h1>
            <h2
              class="text-pretty text-5xl font-bold leading-tight tracking-tight text-muted-foreground sm:text-6xl lg:text-7xl"
            >
              Web Developer
            </h2>
          </div>

          <!-- Tech badges -->
          <div
            class="flex flex-wrap items-center justify-center gap-3 pt-4 max-w-lg"
          >
            <span
              v-for="tech in techs"
              :key="tech"
              class="rounded-full border border-border bg-background/50 px-4 py-1.5 text-sm font-medium text-foreground/80 backdrop-blur-sm"
            >
              {{ tech }}
            </span>
          </div>

          <!-- CTA -->
          <div class="flex items-center justify-center gap-4 pt-8">
            <button
              class="rounded-full bg-foreground px-8 py-3 text-base font-semibold text-background transition-all hover:scale-105 hover:shadow-lg"
            >
              View Projects
            </button>
            <button
              class="rounded-full border-2 border-foreground/20 bg-transparent px-8 py-3 text-base font-semibold text-foreground transition-all hover:border-foreground/40 hover:bg-foreground/5"
            >
              Contact
            </button>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
