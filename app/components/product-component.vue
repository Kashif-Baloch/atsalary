<template>
  <div class="bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 mt-20 py-12 lg:py-20">
      <div class="flex flex-wrap lg:flex-row flex-col-reverse gap-12">
        <div class="flex-1 md:p-4">
          <h1
            class="text-3xl lg:text-5xl font-bold text-white mb-4 leading-tight"
          >
            Maak van salarisadministratie
            <span class="text-blue-700 underline">eenvoud en zekerheid</span>
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            Met @Salary beheer je je volledige salarisadministratie online snel, foutloos en altijd volgens de laatste wet- en regelgeving.
Automatiseer processen, krijg realtime inzicht in loonkosten en werk efficiënter dan ooit, allemaal in één krachtig dashboard.
            
            
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-chart-line text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Realtime inzicht
                </span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-users text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Naadloze koppelingen</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-cog text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Slimme automatisering</span
              >
            </li>
          </ul>
          <Button
            label="Bekijk Demo"
            rounded
            size="large"
            class="mt-12 !bg-blue-700 !text-white !border-none !outline-none"
            @click="handleStartTrial"
          />
        </div>

        <div class="flex-1 text-start">
          <div
            class="bg-blue-400/10 rounded-2xl p-4 md:p-8 max-w-md lg:max-w-xl mx-auto shadow-2xl"
          >
            <h2 class="text-2xl font-bold text-white mb-6">Belangrijkste functies</h2>

            <div class="space-y-6">
              <!-- Feature 1 -->
              <div class="bg-blue-400/10 rounded-xl p-6">
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-blue-700 rounded-full p-2">
                    <i class="pi pi-share-alt text-white text-lg"></i>
                  </div>
                  <h3 class="text-lg font-semibold text-white">
                    Koppelingen met alle boekhoudpakketten
                  </h3>
                </div>
                <p class="text-gray-300 text-sm leading-relaxed">
                  Nooit meer dubbel invoeren — alle gegevens worden automatisch gesynchroniseerd.
                  
                </p>
              </div>

              <!-- Feature 2 -->
              <div class="bg-blue-400/10 rounded-xl p-6">
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-blue-700 rounded-full p-2">
                    <i class="pi pi-eye text-white text-lg"></i>
                  </div>
                  <h3 class="text-lg font-semibold text-white">
                    Managementrapportages
                  </h3>
                </div>
                <p class="text-gray-300 text-sm leading-relaxed">
                  Altijd inzicht in kosten, uren en trends voor betere beslissingen.
                  
                </p>
              </div>

              <!-- Feature 3 -->
              <div class="bg-blue-400/10 rounded-xl p-6">
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-blue-700 rounded-full p-2">
                    <i class="pi pi-bolt text-white text-lg"></i>
                  </div>
                  <h3 class="text-lg font-semibold text-white">
                    Geautomatiseerde loonruns
                  </h3>
                </div>
                <p class="text-gray-300 text-sm leading-relaxed">
                  Loonruns verlopen zoveel mogelijk automatisch, waardoor er nauwelijks handmatige mutaties nodig zijn. Dat bespaart tijd, voorkomt fouten en versnelt het proces.
                  
                </p>
              </div>
            </div>

            <div
              class="mt-8 pt-6 border-t border-blue-50/50 dark:border-blue-400/10"
            >
              <div class="flex justify-between items-center">
                <div class="text-center">
                  <p class="text-2xl font-bold text-white">0</p>
                  <p class="text-gray-400 text-sm">Tevreden klanten</p>
                </div>
                <div class="text-center">
                  <p class="text-2xl font-bold text-white">99.9%</p>
                  <p class="text-gray-400 text-sm">Uptime</p>
                </div>
                <div class="text-center">
                  <p class="text-2xl font-bold text-white">12/7</p>
                  <p class="text-gray-400 text-sm">Ondersteuning</p>
                </div>
              </div>
            </div>

            <div class="mt-6">
              <Button
                @click="handleViewDemo"
                label="Vraag Demo aan"
                rounded
                size="large"
                class="w-full !text-white !bg-blue-700 !border-none !outline-none"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Button from "primevue/button";

const handleStartTrial = () => {
  // Handle start trial action
  console.log("Start trial clicked");
  // You can redirect to signup or show trial modal
};

const handleViewDemo = () => {
  // Handle view demo action
  console.log("View demo clicked");
  // You can open demo modal or redirect to demo page
};
</script>
