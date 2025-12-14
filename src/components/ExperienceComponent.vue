<template>
  <section id="experience" class="py-20">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Title -->
      <div data-aos="fade-up">
        <h2 class="text-4xl md:text-5xl font-bold mb-4 text-center">
          Experience
        </h2>
        <div class="h-1 w-20 bg-accent mx-auto mb-12"></div>
      </div>

      <!-- Timeline -->
      <div class="space-y-8">
        <div
          v-for="(exp, idx) in experiences"
          :key="idx"
          data-aos="fade-right"
          :data-aos-delay="idx * 100"
          class="relative pl-8 border-l-2 border-primary pb-8"
        >
          <!-- Dot -->
          <div
            class="absolute -left-4 top-0 w-6 h-6 bg-primary rounded-full border-4 border-background"
          ></div>

          <!-- Card -->
          <div class="bg-card p-6 rounded-xl border border-border">
            <div
              class="flex flex-col md:flex-row md:justify-between md:items-start mb-4"
            >
              <div>
                <h3 class="text-2xl font-bold text-foreground">
                  {{ exp.role }}
                </h3>
                <p class="text-primary font-semibold">
                  {{ exp.company }}
                </p>
              </div>
              <span class="text-muted-foreground text-sm mt-2 md:mt-0">
                {{ exp.duration }}
              </span>
            </div>

            <div class="space-y-2">
              <p class="font-semibold text-foreground text-sm">
                Responsibility:
              </p>
              <ul class="space-y-1">
                <li
                  v-for="(responsibility, achIdx) in exp.responsibility"
                  :key="achIdx"
                  class="flex items-center gap-2 text-muted-foreground text-sm"
                >
                  <span class="w-2 h-2 bg-accent rounded-full"></span>
                  {{ responsibility }}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const experiences = [
  {
    role: "NOC Fiberization & IP Core",
    company: "PT Ultra Mandiri Telekomunikasi",
    duration: "2023 - Present",
    responsibility: [
      "Report summary and documentation team progress to customer and for manage maintaining Service Level Agreements (SLA)",
      "Escalation Trouble Ticket to team area",
      "Analyzing Fiber Cuts with Ring Topology and Receive Signal Level",
      "Configure PPPOE for new Customer Internet to the Home",
    ],
  },
  {
    role: "Lead Maintenance Operation",
    company: "PT Ultra Mandiri Telekomunikasi",
    duration: "2022 - 2023",
    responsibility: [
      "Manage team schedules and daily reports for preventive and corrective maintenance",
      "Responsible for and managing all petty cash expenses each month",
      "Supervise and monitor the team's performance in properly maintaining Service Level Agreements (SLA).",
    ],
  },
  {
    role: "Maintenance Engineer",
    company: "PT Ultra Mandiri Telekomunikasi",
    duration: "2020 - 2022",
    responsibility: [
      "Carry out preventive and corrective maintenance properly so that service level agreements are maintained",
      "Analyzing fiber cuts using measuring tools such as OTDR and OPM",
    ],
  },
  {
    role: "Project Field Engineer",
    company: "PT Ultra Mandiri Telekomunikasi",
    duration: "2019 - 2020",
    responsibility: [
      "Coordinating permits with the local government and landlord for the smoothness and continuity of project activities",
      "Carry out electrical and physical Acceptance Test Procedures (ATP) at the site with Clients",
    ],
  },
];
</script>
