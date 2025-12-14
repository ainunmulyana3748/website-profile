<template>
  <section id="projects" class="py-20 bg-card/50">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Heading -->
      <div data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold mb-4 text-center">
          Portofolio <span class="text-primary">Projects</span>
        </h2>
        <div class="h-1 w-20 bg-accent mx-auto mb-12"></div>
      </div>

      <!-- Grid -->
      <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
        <div
          v-for="data in projects"
          :key="data.id"
          class="flex flex-col h-full rounded-xl bg-base-100 border border-base-300 shadow-xl transition-all hover:-translate-y-1 hover:shadow-2xl"
        >
          <!-- Image -->
          <div class="relative h-56 overflow-hidden rounded-t-xl">
            <img
              :src="data.image"
              :alt="data.title"
              class="w-full h-full object-cover transition-transform duration-300 hover:scale-105"
            />
          </div>

          <!-- Content -->
          <div class="flex flex-col flex-1 p-5">
            <h6 class="text-xl font-semibold text-base-content mb-2">
              {{ data.title }}
            </h6>

            <p class="text-base-content/80 text-sm leading-relaxed mb-4">
              {{ data.description }}
            </p>

            <!-- Tags -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span
                v-for="tag in data.tags"
                :key="tag"
                class="px-3 py-1 text-xs bg-primary/10 text-primary rounded-full"
              >
                {{ tag }}
              </span>
            </div>

            <!-- Actions -->
            <div class="mt-auto flex gap-3">
              <a
                :href="data.link"
                target="_blank"
                class="flex-1 flex text-white items-center justify-center gap-2 rounded-lg bg-primary px-3 py-2 text-sm font-medium text-primary-foreground hover:bg-primary/90 transition"
              >
                <ExternalLink :size="16" />
                Demo
              </a>

              <a
                :href="data.code"
                target="_blank"
                class="flex-1 flex items-center justify-center gap-2 rounded-lg border border-primary px-3 py-2 text-sm font-medium text-primary hover:bg-primary/10 transition"
              >
                <Github :size="16" />
                Code
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ExternalLink, Github } from "lucide-vue-next";
import Dolandolan from "../assets/img/dolandolan.jpeg";
import Edspert from "../assets/img/Edspert.jpeg";
import House from "../assets/img/house.jpeg";
import CarRental from "../assets/img/car-rental.jpeg";
import BellaVista from "../assets/img/bella-vista.jpeg";
import Dimasakin from "../assets/img/Dimasakin.jpeg";

const projects = [
  {
    id: 1,
    title: "Dolandolan.com",
    description: "Website Holiday for booking ticket",
    image: Dolandolan,
    tags: ["React", "Tailwindcss", "Shadcn", "Swiper"],
    link: "https://dolandolancom.vercel.app",
    code: "https://github.com/ainunmulyana3748/fianl-project-dibimbing",
  },
  {
    id: 2,
    title: "Company Profile",
    description: "Company Profile",
    image: Edspert,
    tags: ["React", "Tailwind"],
    link: "https://final-project-edspert-henna.vercel.app/index.html",
    code: "https://github.com/ainunmulyana3748/final-project-edspert",
  },
  {
    id: 3,
    title: "Website House",
    description: "Webiste Company Profile",
    image: House,
    tags: ["React", "TypeScript", "PostgreSQL", "Redux"],
    link: "https://landing-page-house-six.vercel.app/",
    code: "https://github.com/ainunmulyana3748/LandingPageHouse",
  },
  {
    id: 4,
    title: "Car Rental",
    description: "Website for Booking a Car",
    image: CarRental,
    tags: ["React", "Bootstrap"],
    link: "https://23001028-14-kel2-car-rental-platinum-customer.vercel.app/#carouselExampleIndicators2",
    code: "#",
  },
  {
    id: 5,
    title: "Bella Vista",
    description: "Website for Order Food in Restaurant Bella Vista",
    image: BellaVista,
    tags: ["React", "Tailwindcss", "Shadcn", "Supabase"],
    link: "https://bella-vista-seven.vercel.app/",
    code: "https://github.com/ainunmulyana3748/UAS_PBW",
  },
  {
    id: 6,
    title: "Dimasakin",
    description: "Website for Order Food",
    image: Dimasakin,
    tags: ["React", "Tailwindcss", "Shadcm"],
    link: "https://dimasakin.vercel.app/",
    code: "https://github.com/ainunmulyana3748/web-food-next-project",
  },
];
</script>
