<template>
  <div class="bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 mt-20 py-12 lg:py-20">
      <div class="flex flex-wrap lg:flex-row flex-col-reverse gap-12">
        <div class="flex-1 md:p-4">
          <h1
            class="lg:text-5xl text-3xl font-bold text-white mb-4 leading-tight"
          >
            Wij helpen bedrijven groeien met
            <span class="text-blue-700 underline">slimme salarisinnovatie</span>
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            Sinds 2025 ontwikkelen wij krachtige salarisadministratie-oplossingen die bedrijven helpen om foutloos te werken, altijd compliant te blijven en realtime inzicht te krijgen in hun personeelskosten.
            
            
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-heart text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Passie voor efficiëntie</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-lightbulb text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Innovatieve oplossingen</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-shield text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Betrouwbare partner</span
              >
            </li>
          </ul>
          <Button
            label="Ontmoet Ons Team"
            rounded
            size="large"
            class="mt-12 !bg-blue-700 !text-white !border-none !outline-none"
            @click="handleMeetTeam"
          />
        </div>

        <div class="flex-1 text-start">
          <div
            class="bg-blue-400/10 rounded-2xl p-8 max-w-md lg:max-w-xl mx-auto shadow-2xl"
          >
            <h2 class="text-2xl font-bold text-white mb-6">Ons Verhaal</h2>

            <div class="space-y-6">
              <!-- Mission -->
              <div class="bg-blue-400/10 rounded-xl p-6">
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-blue-700 rounded-full p-2">
                    <i class="pi pi-flag text-white text-lg"></i>
                  </div>
                  <h3 class="text-lg font-semibold text-white">Onze Missie</h3>
                </div>
                <p class="text-gray-300 text-sm leading-relaxed">
                  Bedrijven in staat stellen hun salarisadministratie volledig te automatiseren, zodat zij zich kunnen richten op groei en hun medewerkers op tevredenheid.
                  
                  
                </p>
              </div>

              <!-- Vision -->
              <div class="bg-blue-400/10 rounded-xl p-6">
                <div class="flex items-center gap-3 mb-3">
                  <div class="bg-blue-700 rounded-full p-2">
                    <i class="pi pi-star text-white text-lg"></i>
                  </div>
                  <h3 class="text-lg font-semibold text-white">Onze Visie</h3>
                </div>
                <p class="text-gray-300 text-sm leading-relaxed">
                  Een wereld waarin elk bedrijf groot of klein eenvoudig, foutloos en volledig volgens de regels salaris kan uitbetalen.
                  
                </p>
              </div>
            </div>

            <div
              class="mt-8 pt-6 border-t border-blue-50/50 dark:border-blue-400/10"
            >
              <div class="flex justify-between items-center">
                <div class="text-center">
                  <p class="text-2xl font-bold text-white">1+</p>
                  <p class="text-gray-400 text-sm">Jaar Ervaring</p>
                </div>
                <div class="text-center">
                  <p class="text-2xl font-bold text-white">5+</p>
                  <p class="text-gray-400 text-sm">Team Leden</p>
                </div>
                <div class="text-center">
                  <p class="text-2xl font-bold text-white">100%</p>
                  <p class="text-gray-400 text-sm">Toegewijd</p>
                </div>
              </div>
            </div>

            <div class="mt-6">
              <Button
                @click="handleViewLocation"
                label="Onze Locatie"
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

const handleMeetTeam = () => {
  // Handle meet team action
  console.log("Meet team clicked");
  // You can redirect to team page or show team modal
};

const handleViewLocation = () => {
  // Handle view location action
  console.log("View location clicked");
  // You can show map or redirect to contact page with address
};
</script>
