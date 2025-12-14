<template>
  <footer>
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
      <div class="grid md:grid-cols-4 gap-8 mb-8">
        <div>
          <h3 class="text-lg font-bold text-base-content mb-4">Portfolio</h3>
          <p class="text-base-content/70 text-sm">
            Membangun pengalaman digital yang luar biasa dengan teknologi
            terkini.
          </p>
        </div>

        <div>
          <h4 class="font-semibold text-base-content mb-4">Navigation</h4>
          <ul class="space-y-2 text-sm text-base-content/70">
            <li>
              <a href="#home" class="hover:text-primary transition-colors">
                Home
              </a>
            </li>
            <li>
              <a
                href="#experience"
                class="hover:text-primary transition-colors"
              >
                Experience
              </a>
            </li>
            <li>
              <a href="#projects" class="hover:text-primary transition-colors">
                Projects
              </a>
            </li>
            <li>
              <a href="#contact" class="hover:text-primary transition-colors">
                Contact
              </a>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="font-semibold text-base-content mb-4">Services</h4>
          <ul class="space-y-2 text-sm text-base-content/70">
            <li>
              <a href="#" class="hover:text-primary transition-colors">
                Web Development
              </a>
            </li>
            <li>
              <a href="#" class="hover:text-primary transition-colors">
                App Development
              </a>
            </li>
            <li>
              <a href="#" class="hover:text-primary transition-colors">
                Consulting
              </a>
            </li>
            <li>
              <a href="#" class="hover:text-primary transition-colors">
                Design
              </a>
            </li>
          </ul>
        </div>

        <div>
          <h4 class="font-semibold text-base-content mb-4">Social</h4>
          <div class="flex gap-3">
            <a
              href="#"
              class="p-2 bg-base-300 rounded-lg text-base-content hover:bg-primary hover:text-primary-content transition-colors"
            >
              <Github :size="20" />
            </a>
            <a
              href="#"
              class="p-2 bg-base-300 rounded-lg text-base-content hover:bg-primary hover:text-primary-content transition-colors"
            >
              <Linkedin :size="20" />
            </a>
            <a
              href="#"
              class="p-2 bg-base-300 rounded-lg text-base-content hover:bg-primary hover:text-primary-content transition-colors"
            >
              <Twitter :size="20" />
            </a>
            <a
              href="#"
              class="p-2 bg-base-300 rounded-lg text-base-content hover:bg-primary hover:text-primary-content transition-colors"
            >
              <Mail :size="20" />
            </a>
          </div>
        </div>
      </div>

      <div
        class="border-t border-base-300 pt-8 flex flex-col md:flex-row justify-between items-center text-sm text-base-content/70"
      >
        <p>&copy; 2025 Ainun Mulyana. All rights reserved.</p>
        <div class="flex gap-6 mt-4 md:mt-0">
          <a href="#" class="hover:text-primary transition-colors">
            Privacy Policy
          </a>
          <a href="#" class="hover:text-primary transition-colors">
            Terms of Service
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Github, Linkedin, Twitter, Mail } from "lucide-vue-next";
</script>
