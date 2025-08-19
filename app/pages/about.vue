<template>
  <Navbar />

  <OveronsComponent />

  <div class="min-h-screen bg-surface-900">
    <!-- Hero -->
    <section>
      <div class="container mx-auto max-w-7xl px-4 py-16 md:py-20">
        <p class="text-blue-700 uppercase tracking-wider font-semibold">
          Over ons
        </p>
        <h1
          class="mt-3 text-4xl md:text-5xl font-bold text-white leading-tight"
        >
          Mensen maken @Salary
        </h1>
        <p class="mt-4 text-surface-400 max-w-3xl">
          We bouwen salarisoplossingen die organisaties vereenvoudigen en teams
          versterken. Leer ons leadership kennen en ontdek de afdelingen die dat
          elke dag waarmaken.
        </p>
      </div>
    </section>

    <!-- Tabs: Afdelingen -->
    <section class="container mx-auto max-w-7xl px-4 py-8 md:py-10">
      <div class="w-full overflow-x-auto">
        <div
          class="inline-flex gap-2 rounded-xl border border-surface-800 p-1 bg-surface-900"
        >
          <button
            v-for="tab in tabs"
            :key="tab.key"
            @click="activeTab = tab.key"
            class="px-4 md:px-5 py-2 rounded-lg text-sm md:text-base transition-colors"
            :class="
              activeTab === tab.key
                ? 'bg-surface-800 text-surface-0'
                : 'text-surface-300 hover:bg-surface-800/60'
            "
          >
            {{ tab.label }}
          </button>
        </div>
      </div>
    </section>

    <!-- People grid -->
    <section class="container mx-auto max-w-7xl px-4 py-10 md:py-12">
      <div class="flex items-center justify-between mb-6">
        <h2 class="text-2xl md:text-3xl font-semibold text-surface-0">
          {{ currentLabel }}
        </h2>
        <div class="text-sm text-surface-400">
          {{ filteredPeople.length }} personen
        </div>
      </div>

      <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
        <article
          v-for="person in filteredPeople"
          :key="person.id"
          class="rounded-2xl border border-surface-800 bg-surface-900 p-5 hover:border-blue-700/50 transition-colors"
        >
          <div class="flex items-center gap-4">
            <div
              class="w-14 h-14 rounded-xl bg-surface-800 grid place-content-center text-lg font-semibold text-surface-200"
            >
              {{ person.initials }}
            </div>
            <div>
              <h3 class="text-base font-medium text-surface-0">
                {{ person.name }}
              </h3>
              <p class="text-sm text-blue-700">
                {{ person.role }}
              </p>
            </div>
          </div>
          <p class="mt-4 text-sm text-surface-400">
            {{ person.bio }}
          </p>
          <div class="mt-5 flex items-center gap-3 text-surface-500">
            <i v-if="person.links?.linkedin" class="pi pi-linkedin"></i>
            <i v-if="person.links?.x" class="pi pi-twitter"></i>
            <i v-if="person.links?.github" class="pi pi-github"></i>
          </div>
        </article>
      </div>
    </section>

    <!-- Waarden -->
    <section class="container mx-auto max-w-7xl px-4 py-12">
      <div class="text-center max-w-3xl mx-auto">
        <h2 class="text-2xl md:text-3xl font-semibold text-surface-0">
          Onze waarden
        </h2>
        <p class="mt-3 text-surface-400">
          De principes die ons dagelijks sturen van productbeslissingen tot
          support.
        </p>
      </div>

      <div class="mt-10 grid gap-6 md:grid-cols-3">
        <div class="rounded-2xl border border-surface-800 bg-surface-900 p-6">
          <i class="pi pi-star text-xl text-[#d6af84]"></i>
          <h3 class="mt-3 font-medium text-surface-0">Klantwaarde eerst</h3>
          <p class="mt-2 text-surface-400 text-sm">
            We leveren features die echte impact hebben meetbaar en merkbaar
          </p>
        </div>
        <div class="rounded-2xl border border-surface-800 bg-surface-900 p-6">
          <i class="pi pi-shield text-xl text-[#d6af84]"></i>
          <h3 class="mt-3 font-medium text-surface-0">Betrouwbaarheid</h3>
          <p class="mt-2 text-surface-400 text-sm">
            Veilig, voorspelbaar en schaalbaar. Payroll laat geen ruimte voor
            toeval
          </p>
        </div>
        <div class="rounded-2xl border border-surface-800 bg-surface-900 p-6">
          <i class="pi pi-bolt text-xl text-[#d6af84]"></i>
          <h3 class="mt-3 font-medium text-surface-0">Eigenaarschap</h3>
          <p class="mt-2 text-surface-400 text-sm">
            Kleine teams, grote verantwoordelijkheid iedereen maakt het
            verschil
          </p>
        </div>
      </div>
    </section>

    <!-- CTA -->
    <section class="container mx-auto max-w-7xl px-4 py-12">
      <div
        class="rounded-2xl overflow-hidden relative border border-surface-800 bg-surface-900"
        style="
          background: radial-gradient(
            120% 100% at 100% 0%,
            color-mix(in srgb, var(--p-blue-700), transparent 40%) 0%,
            var(--p-surface-900) 60%
          );
        "
      >
        <div class="p-8 md:p-12">
          <p class="text-blue-700 uppercase tracking-wider font-semibold">
            Word collega
          </p>
          <h3 class="mt-3 text-2xl md:text-3xl font-semibold text-white">
            Kom bouwen aan de toekomst van payroll
          </h3>
          <p class="mt-2 text-surface-400 max-w-2xl">
            We zoeken engineers, product thinkers en klanthelden. Zie je jezelf
            erbij?
          </p>
          <div class="mt-6 flex items-center gap-3">
            <Button
              label="Openstaande vacatures"
              class="!bg-blue-700 !outline-none !border-none !text-white"
              rounded
            />
            <NuxtLink
              to="/contact"
              class="text-blue-700 hover:text-blue-600 transition-colors"
              >Of neem contact op →</NuxtLink
            >
          </div>
        </div>
        <img
          src="https://fqjltiegiezfetthbags.supabase.co/storage/v1/render/image/public/block.images/blocks/cta/mockup.png"
          alt=""
          class="hidden md:block absolute -right-6 -top-10 h-80 pointer-events-none select-none opacity-90"
        />
      </div>
    </section>
  </div>

  <Footer />
</template>

<script setup>
import { ref, computed } from "vue";
import Button from "primevue/button";
import Navbar from "../layouts/navbar.vue";
import Footer from "../layouts/footer.vue";
import OveronsComponent from "../components/overons-component.vue";
import { useHead } from "#imports";

useHead({
  title: "Over ons — @Salary",
  meta: [
    { name: "description", content: "Maak kennis met het team achter @Salary" },
  ],
});

const tabs = [
  { key: "leadership", label: "Management" },
  { key: "engineering", label: "Engineering" },
  { key: "sales", label: "Sales" },
  { key: "support", label: "Support" },
  { key: "hr", label: "HR & Finance" },
];
const activeTab = ref("leadership");

const people = {
  leadership: [
    {
      id: 1,
      initials: "AV",
      name: "Anouk Vermeer",
      role: "CEO",
      bio: "Ex-consultant, productgedreven leider met focus op klantwaarde.",
      links: { linkedin: true },
    },
    {
      id: 2,
      initials: "JB",
      name: "Jasper Brouwer",
      role: "CTO",
      bio: "Architect van onze schaalbare payroll-infra.",
      links: { linkedin: true, github: true },
    },
    {
      id: 3,
      initials: "LS",
      name: "Lotte Smits",
      role: "CPO",
      bio: "Eenvoudige flows, krachtige automatisering.",
      links: { linkedin: true },
    },
    {
      id: 4,
      initials: "MV",
      name: "Mees van Dijk",
      role: "CFO",
      bio: "Datagedreven besluitvorming en duurzame groei.",
      links: { linkedin: true },
    },
  ],
  engineering: [
    {
      id: 11,
      initials: "KD",
      name: "Kim de Ruiter",
      role: "Staff Engineer",
      bio: "API-first, security by default.",
      links: { github: true },
    },
    {
      id: 12,
      initials: "RT",
      name: "Ravi Tjin",
      role: "Senior Backend",
      bio: "Betrouwbare uitbetalingen, elke run.",
      links: { github: true },
    },
    {
      id: 13,
      initials: "EF",
      name: "Eva Faber",
      role: "Frontend Engineer",
      bio: "Heldere UI’s met performance in de lead.",
      links: { x: true },
    },
    {
      id: 14,
      initials: "YO",
      name: "Yara Ouwehand",
      role: "QA Lead",
      bio: "Nauwkeurigheid in elke flow.",
      links: { linkedin: true },
    },
  ],
  sales: [
    {
      id: 21,
      initials: "BM",
      name: "Bram Meijer",
      role: "Head of Sales",
      bio: "Luisteren → begrijpen → oplossen.",
      links: { linkedin: true },
    },
    {
      id: 22,
      initials: "ND",
      name: "Noa Dekker",
      role: "Account Executive",
      bio: "Van demo naar waarde in weken.",
      links: { linkedin: true },
    },
    {
      id: 23,
      initials: "TZ",
      name: "Tess Zwart",
      role: "SDR",
      bio: "De juiste vraag maakt het verschil.",
      links: { x: true },
    },
  ],
  support: [
    {
      id: 31,
      initials: "IH",
      name: "Ilias Hamed",
      role: "Support Lead",
      bio: "Snel, vriendelijk en oplossingsgericht.",
      links: { linkedin: true },
    },
    {
      id: 32,
      initials: "PV",
      name: "Puck Verhoeven",
      role: "Customer Success",
      bio: "Proactief en meetbare adoptie.",
      links: { linkedin: true },
    },
  ],
  hr: [
    {
      id: 41,
      initials: "GS",
      name: "Gwen S.",
      role: "Head of People",
      bio: "Sterke teams met duidelijke doelen.",
      links: { linkedin: true },
    },
    {
      id: 42,
      initials: "DR",
      name: "Daan R.",
      role: "Finance Controller",
      bio: "Transparantie en voorspelbaarheid.",
      links: { linkedin: true },
    },
  ],
};

const filteredPeople = computed(() => people[activeTab.value] || []);
const currentLabel = computed(
  () => tabs.find((t) => t.key === activeTab.value)?.label ?? "Team"
);

const stats = [
  { label: "Klanten", value: "1.2k+" },
  { label: "Landen", value: "6" },
  { label: "SLA uptime", value: "99.95%" },
  { label: "Teamleden", value: "40+" },
];
</script>
