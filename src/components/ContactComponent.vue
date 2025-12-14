<template>
  <section id="contact" class="py-20">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div data-aos="fade-up">
        <h2
          class="text-4xl md:text-5xl font-bold mb-4 text-center text-base-content"
        >
          Hubungi <span class="text-primary">Saya</span>
        </h2>
        <div class="h-1 w-20 bg-primary mx-auto mb-12"></div>
      </div>

      <div class="grid md:grid-cols-2 gap-12">
        <div data-aos="fade-right">
          <h3 class="text-2xl font-bold mb-8 text-base-content">
            Mari Terhubung
          </h3>

          <div class="space-y-8">
            <div class="flex gap-4">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-lg bg-primary text-primary-content"
                >
                  <Mail :size="24" />
                </div>
              </div>
              <div>
                <h4 class="text-lg font-semibold text-base-content">Email</h4>
                <p class="text-base-content/70">ainun3748@gmail.com</p>
              </div>
            </div>

            <div class="flex gap-4">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-lg bg-primary text-primary-content"
                >
                  <Phone :size="24" />
                </div>
              </div>
              <div>
                <h4 class="text-lg font-semibold text-base-content">Phone</h4>
                <p class="text-base-content/70">+62 813 1497 5525</p>
              </div>
            </div>

            <div class="flex gap-4">
              <div class="flex-shrink-0">
                <div
                  class="flex items-center justify-center h-12 w-12 rounded-lg bg-primary text-primary-content"
                >
                  <MapPin :size="24" />
                </div>
              </div>
              <div>
                <h4 class="text-lg font-semibold text-base-content">Lokasi</h4>
                <p class="text-base-content/70">Jakarta, Indonesia</p>
              </div>
            </div>
          </div>
        </div>

        <div
          data-aos="fade-left"
          class="bg-base-100 p-8 rounded-xl shadow-lg border border-base-300"
        >
          <form class="space-y-6">
            <div>
              <label class="block text-sm font-semibold mb-2 text-base-content"
                >Nama</label
              >
              <input
                type="text"
                name="name"
                class="input input-bordered w-full text-base-content transition-colors"
                placeholder="Nama Anda"
                required
              />
            </div>

            <div>
              <label class="block text-sm font-semibold mb-2 text-base-content"
                >Email</label
              >
              <input
                type="email"
                name="email"
                class="input input-bordered w-full text-base-content transition-colors"
                placeholder="email@example.com"
                required
              />
            </div>

            <div>
              <label class="block text-sm font-semibold mb-2 text-base-content"
                >Pesan</label
              >
              <textarea
                name="message"
                rows="5"
                class="textarea textarea-bordered w-full text-base-content transition-colors resize-none"
                placeholder="Tulis pesan Anda di sini..."
                required
              ></textarea>
            </div>

            <button
              type="submit"
              class="btn btn-primary w-full font-semibold flex items-center justify-center gap-2"
            >
              <Send :size="20" />
              Kirim Pesan
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { Mail, Phone, MapPin, Send } from "lucide-vue-next";
</script>
