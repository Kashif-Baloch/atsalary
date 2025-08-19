<template>
  <Navbar />

  <div class="bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 mt-20 py-12 lg:py-20">
      <div class="flex flex-wrap lg:flex-row flex-col-reverse gap-12">
        <div class="flex-1 md:p-4">
          <h1
            class="lg:text-5xl text-3xl font-bold text-white mb-4 leading-tight"
          >
            Eén tarief per medewerker,
            <span class="text-blue-700 underline">geen verborgen kosten</span>
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            Alles wat je nodig hebt om je salarisadministratie foutloos, snel en volledig online te regelen. Geen verborgen kosten, één vast bedrag per maand.
            
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-check text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Volledig geautomatiseerde loonruns minder handmatig werk, altijd foutloos</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-check text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Koppelingen met alle boekhoudpakketten nooit meer dubbel invoeren</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-check text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Realtime rapportages & inzichten direct overzicht in loonkosten en uren</span
              >
            </li>
          </ul>
          <Button
            label="Klant worden?"
            rounded
            size="large"
            class="mt-12 !text-white !bg-blue-700 !border-none !outline-none"
            @click="handleGetStarted"
          />
        </div>

        <div class="flex-1">
          <div
            class="bg-blue-400/10 rounded-2xl p-8 max-w-md lg:max-w-xl mx-auto shadow-2xl border-2 border-blue-700"
          >
            <div class="text-center mb-6">
              <div
                class="inline-block bg-blue-700 text-white px-4 py-2 rounded-full text-sm font-medium mb-4"
              >
                Een transparant pakket
              </div>
              <h2 class="text-3xl font-bold text-white mb-2">
                Compleet @Salary Pakket
              </h2>
              <div class="flex items-center justify-center gap-2">
                <span class="text-5xl font-bold text-blue-700">€15,00</span>
                <span class="text-gray-400 text-lg">/p.m.p.m</span>
              </div>
            </div>

            <div class="space-y-6 mb-8">
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Geautomatiseerde loonruns</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Boekhoudkoppelingen</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Uren-, verlof- en declaratiebeheer</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Realtime rapportages</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Onbetaalde ondersteuning</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">API-toegang</span>
              </div>
            </div>

            <Button
              label="We gaan ervoor"
              rounded
              size="large"
              class="w-full !text-white !bg-blue-700 !border-none !outline-none mb-4"
              @click="handleChoosePlan"
            />

            <div class="mt-6 pt-6 border-t border-gray-700">
              <div class="text-center">
                <p class="text-gray-400 text-sm mb-2">Hulp nodig ?</p>
                <div class="flex justify-center space-x-4">
                  <a href="#" class="text-gray-400 text-sm transition-colors">
                    <i class="pi pi-phone mr-1 text-[#d6af84]"></i>Neem contact op per telefoon
                  </a>
                  <a href="#" class="text-gray-400 text-sm transition-colors">
                    <i class="pi pi-envelope mr-1 text-[#d6af84]"></i>Neem contact op per mail
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <Footer />
</template>

<script setup>
import Button from "primevue/button";
import Navbar from "~/layouts/navbar.vue";
import Footer from "~/layouts/footer.vue";

useHead({
  title: "Pricing — @Salary",
  meta: [{ name: "description", content: "Social CRM platform" }],
});

const handleGetStarted = () => {
  // Handle get started action
  console.log("Get started clicked");
  // You can redirect to signup or show a modal
};

const handleChoosePlan = () => {
  // Handle plan selection
  console.log("Plan selected: Complete CRM Package - €30/month");
  // You can redirect to payment or show checkout modal
};
</script>
