<template>
  <Navbar />

  <ProductComponent />

  <div class="bg-surface-900">
    <div
      class="container mx-auto max-w-7xl px-4 py-20 flex flex-col gap-8 justify-center items-center relative"
    >
      <div class="flex flex-col gap-2 items-center max-w-3xl mx-auto">
        <h3 class="text-surface-0 font-bold text-2xl leading-tight text-center">
          Ontdek de functies
        </h3>
        <p class="text-surface-400 text-center leading-tight">
          Met @Salary beheer je al je salarisgerelateerde processen op één plek. Van declaraties tot verlof en loonruns alles is snel, foutloos en overzichtelijk geregeld.
          
        </p>
      </div>

      <div class="mx-auto">
        <div class="xl:hidden flex flex-col gap-12">
          <div
            v-for="(item, index) in timelineItems"
            :key="index"
            class="grid grid-cols-1 sm:grid-cols-[42px_1fr] gap-4"
          >
            <div class="hidden sm:flex flex-col items-center">
              <div
                class="w-12 h-12 rounded-2xl border border-surface-700 flex items-center justify-center px-1 py-2 bg-surface-800"
              >
                <span
                  class="text-surface-0 font-medium text-xl leading-tight"
                  >{{ item.id }}</span
                >
              </div>
              <div class="w-px bg-surface-700 flex-1" />
            </div>
            <div class="flex w-full flex-col gap-4">
              <div
                class="w-fit h-52 bg-surface-800 rounded-[10px] overflow-hidden flex justify-center items-center shadow-inner relative"
              >
                <img
                  :src="`/archief/${item.id}.png`"
                  :alt="`Image ${item.id}`"
                  class="w-full h-full object-cover"
                />
              </div>
              <div class="flex flex-col gap-4">
                <div class="flex flex-col gap-2">
                  <h4 class="text-surface-0 text-lg font-medium leading-tight">
                    {{ item.title }}
                  </h4>
                  <p class="text-surface-400 leading-normal">
                    {{ item.description }}
                  </p>
                </div>
                <div class="h-px bg-surface-700 w-full" />
                <div class="flex flex-col gap-2">
                  <p
                    v-for="(detail, detailIndex) in item.details"
                    :key="detailIndex"
                    class="leading-normal text-surface-0"
                  >
                    <span class="font-medium">{{ detail.title }}</span>
                    <span class="text-surface-400">{{ detail.text }}</span>
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="hidden xl:flex flex-col gap-12">
          <div
            v-for="(item, index) in timelineItems"
            :key="index"
            class="flex gap-12"
            :class="{ 'flex-row-reverse': index % 2 === 0 }"
          >
            <div class="w-127">
              <div
                class="h-52 bg-surface-800 rounded-[10px] overflow-hidden flex justify-center items-center shadow-inner relative"
              >
                <div class="w-full h-full flex items-center justify-center">
                  <img
                    :src="`/archief/${item.id}.png`"
                    :alt="`Image ${item.id}`"
                    class="w-full h-full object-cover"
                  />
                </div>
              </div>
            </div>
            <div class="flex flex-col items-center">
              <div
                class="w-12 h-12 rounded-2xl border border-surface-700 flex items-center justify-center px-1 py-2 bg-surface-800"
              >
                <span
                  class="text-surface-0 font-medium text-xl leading-tight"
                  >{{ item.id }}</span
                >
              </div>
              <div class="w-px bg-surface-700 h-[200px]" />
            </div>
            <div class="w-127" :class="{ 'text-right': index % 2 === 0 }">
              <div class="flex flex-col gap-4">
                <div class="flex flex-col gap-2">
                  <h4 class="text-surface-0 text-lg font-medium leading-tight">
                    {{ item.title }}
                  </h4>
                  <p class="text-surface-400 leading-normal">
                    {{ item.description }}
                  </p>
                </div>
                <div class="h-px bg-surface-700 w-full" />
                <div class="flex flex-col gap-2">
                  <p
                    v-for="(detail, detailIndex) in item.details"
                    :key="detailIndex"
                    class="leading-normal text-surface-0"
                  >
                    <span class="font-medium">{{ detail.title }}</span>
                    <span class="text-surface-400">{{ detail.text }}</span>
                  </p>
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
import Navbar from "../layouts/navbar.vue";
import Footer from "../layouts/footer.vue";
import { ref } from "vue";
import ProductComponent from "../components/product-component.vue";

useHead({
  title: "Product — @Salary",
  meta: [{ name: "description", content: "Social CRM platform" }],
});

const timelineItems = ref([
  {
    id: 1,
    title: "Declaratiebeheer",
    description:
      "Dien declaraties digitaal in en keur ze goed met één klik.",
    details: [
      {
        title: "Voordelen: ",
        text: "minder papierwerk, sneller goedkeuren, altijd overzicht.",
      },
    ],
    imageWidth: "23rem",
  },
  {
    id: 2,
    title: "Verlofbeheer",
    description:
      "Altijd inzicht in verlofaanvragen en -saldi.",
    details: [
      {
        title: "Voordelen: ",
        text: "realtime saldo, één-klik goedkeuring, automatische koppeling met salaris.",
      },
    ],
    imageWidth: "14rem",
  },
  {
    id: 3,
    title: "Geautomatiseerde loonruns",
    description:
      "Voer loonruns automatisch uit met minimale mutaties.",
    details: [
      {
        title: "Voordelen: ",
        text: "tijdbesparing, foutloos, altijd up-to-date volgens wetgeving.",
      },
    ],
    imageWidth: "25rem",
  },
]);
</script>
