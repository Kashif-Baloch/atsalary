<template>
  <Navbar />

  <div class="bg-surface-0 dark:bg-surface-900">
    <div
      class="container mx-auto max-w-7xl px-4 mt-20 py-20 flex flex-col gap-8 justify-center items-center relative"
    >
      <div class="flex flex-col gap-2 items-center max-w-3xl mx-auto">
        <h3
          class="text-surface-900 dark:text-surface-0 font-bold text-2xl leading-tight text-center"
        >
          Explore the features
        </h3>
        <p
          class="text-surface-600 dark:text-surface-400 text-center leading-tight"
        >
          Libero justo laoreet sit amet cursus sit amet dictum. Auctor neque
          vitae tempus quam pellentesque nec nam.
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
                class="w-12 h-12 rounded-2xl border border-surface-200 dark:border-surface-700 flex items-center justify-center px-1 py-2 bg-white dark:bg-surface-800"
              >
                <span
                  class="text-surface-900 dark:text-surface-0 font-medium text-xl leading-tight"
                  >{{ item.id }}</span
                >
              </div>
              <div class="w-px bg-surface-200 dark:bg-surface-700 flex-1" />
            </div>
            <div class="flex w-full flex-col gap-4">
              <div
                class="w-full h-52 bg-surface-50 dark:bg-surface-800 rounded-[10px] overflow-hidden flex justify-center items-start shadow-inner relative"
              >
                <img
                  :src="`/archief/Picture ${item.id + 1}.png`"
                  :alt="`Image ${item.id + 1}`"
                  class="max-w-full max-h-full object-contain"
                  style="height: auto"
                />
              </div>
              <div class="flex flex-col gap-4">
                <div class="flex flex-col gap-2">
                  <h4
                    class="text-surface-900 dark:text-surface-0 text-lg font-medium leading-tight"
                  >
                    {{ item.title }}
                  </h4>
                  <p
                    class="text-surface-600 dark:text-surface-400 leading-normal"
                  >
                    {{ item.description }}
                  </p>
                </div>
                <div class="h-px bg-surface-200 dark:bg-surface-700 w-full" />
                <div class="flex flex-col gap-2">
                  <p
                    v-for="(detail, detailIndex) in item.details"
                    :key="detailIndex"
                    class="leading-normal text-surface-900 dark:text-surface-0"
                  >
                    <span class="font-medium">{{ detail.title }}</span>
                    <span class="text-surface-600 dark:text-surface-400">{{
                      detail.text
                    }}</span>
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
                class="h-52 bg-surface-50 dark:bg-surface-800 rounded-[10px] overflow-hidden flex justify-center items-start shadow-inner relative"
              >
                <div class="w-full h-full flex items-center justify-center">
                  <img
                    :src="`/archief/Picture ${item.id + 1}.png`"
                    :alt="`Image ${item.id + 1}`"
                    class="w-full h-full object-contain"
                  />
                </div>
              </div>
            </div>
            <div class="flex flex-col items-center">
              <div
                class="w-12 h-12 rounded-2xl border border-surface-200 dark:border-surface-700 flex items-center justify-center px-1 py-2 bg-white dark:bg-surface-800"
              >
                <span
                  class="text-surface-900 dark:text-surface-0 font-medium text-xl leading-tight"
                  >{{ item.id }}</span
                >
              </div>
              <div class="w-px bg-surface-200 dark:bg-surface-700 h-[200px]" />
            </div>
            <div class="w-127" :class="{ 'text-right': index % 2 === 0 }">
              <div class="flex flex-col gap-4">
                <div class="flex flex-col gap-2">
                  <h4
                    class="text-surface-900 dark:text-surface-0 text-lg font-medium leading-tight"
                  >
                    {{ item.title }}
                  </h4>
                  <p
                    class="text-surface-600 dark:text-surface-400 leading-normal"
                  >
                    {{ item.description }}
                  </p>
                </div>
                <div class="h-px bg-surface-200 dark:bg-surface-700 w-full" />
                <div class="flex flex-col gap-2">
                  <p
                    v-for="(detail, detailIndex) in item.details"
                    :key="detailIndex"
                    class="leading-normal text-surface-900 dark:text-surface-0"
                  >
                    <span class="font-medium">{{ detail.title }}</span>
                    <span class="text-surface-600 dark:text-surface-400">{{
                      detail.text
                    }}</span>
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

const timelineItems = ref([
  {
    id: 1,
    title: "Ornare Arcu Odio",
    description:
      "Quisque sagittis purus sit amet volutpat consequat mauris nunc. Scelerisque eleifend.",
    details: [
      {
        title: "Sed lectus vestibulum",
        text: "mattis ullamcorper velit. Laoreet sit amet cursus sit.",
      },
      {
        title: "Fames ac turpis",
        text: "egestas sed tempus urna et. Cursus turpis massa.",
      },
    ],
    imageWidth: "23rem",
  },
  {
    id: 2,
    title: "A diam maecenas",
    description:
      "Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit.",
    details: [
      {
        title: "Quis hendrerit dolor",
        text: "magna eget est. Pellentesque pulvinar pellentesque.",
      },
      {
        title: "Lectus urna duis",
        text: "convallis convallis tellus id interdum velit laoreet.",
      },
    ],
    imageWidth: "14rem",
  },
  {
    id: 3,
    title: "Pharetra et ultrices neque",
    description:
      "Id interdum velit laoreet id. A iaculis at erat pellentesque adipiscing commodo elit at imperdiet.",
    details: [
      {
        title: "Egestas dui id",
        text: "ornare arcu odio ut. Mi bibendum neque egestas congue.",
      },
      {
        title: "Sed velit dignissim",
        text: "sodales ut eu. Massa placerat duis ultricies lacus.",
      },
    ],
    imageWidth: "25rem",
  },
]);
</script>
