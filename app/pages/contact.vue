<template>
  <Navbar />

  <div class="bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 mt-20 py-12 lg:py-20">
      <div class="flex flex-wrap lg:flex-row flex-col gap-12">
        <div class="flex-1 md:p-4">
          <h1
            class="lg:text-5xl text-3xl font-bold text-white mb-4 leading-tight"
          >
            Neem vandaag nog <span class="text-blue-700 underline">contact</span> met ons op
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            Wij staan klaar om je te helpen. Stuur ons een bericht en ons team reageert zo snel mogelijk
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-phone text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Binnen 24 uur reactie snel antwoord op je vragen</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-envelope text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Toegewijd supportteam deskundige hulp bij elke stap</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-users text-[#d6af84] text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Oplossingen op maat advies dat past bij jouw organisatie</span
              >
            </li>
          </ul>
        </div>

        <div class="flex-1 md:p-4 text-left">
          <div
            class="bg-blue-400/10 rounded-2xl md:p-8 p-4 py-8 md:py-8 lg:max-w-xl mx-auto shadow-2xl"
          >
            <h2 class="text-2xl font-bold text-white mb-6">Contactformulier</h2>
            <form @submit.prevent="handleSubmit" class="space-y-6">
              <div>
                <label
                  class="block text-gray-400 text-sm font-medium mb-2"
                  for="name"
                >
                  Naam
                </label>
                <input
                  v-model="form.name"
                  type="text"
                  id="name"
                  name="name"
                  required
                  class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:border-transparent transition-all"
                  placeholder="Vul je volledige naam in"
                />
              </div>

              <div>
                <label
                  class="block text-gray-400 text-sm font-medium mb-2"
                  for="email"
                >
                  E-mailadres
                </label>
                <input
                  v-model="form.email"
                  type="email"
                  id="email"
                  name="email"
                  required
                  class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:border-transparent transition-all"
                  placeholder="Zodat we je kunnen bereiken"
                />
              </div>

              <div>
                <label
                  class="block text-gray-400 text-sm font-medium mb-2"
                  for="message"
                >
                  Bericht
                </label>
                <textarea
                  v-model="form.message"
                  id="message"
                  name="message"
                  rows="4"
                  required
                  class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:border-transparent transition-all resize-none"
                  placeholder="Vertel ons waar we je mee kunnen helpen"
                ></textarea>
              </div>

              <Button
                type="submit"
                :loading="isSubmitting"
                label="Verstuur bericht"
                rounded
                size="large"
                class="w-full !text-white !bg-blue-700 !border-none !outline-none"
              />
            </form>

            <div class="mt-8 pt-6 border-t border-gray-700">
              <div class="flex justify-center gap-4">
                <div class="text-center">
                  <i
                    class="pi pi-envelope text-[#d6af84] text-lg mb-2 block"
                  ></i>
                  <p class="text-gray-400 text-sm">Email</p>
                  <p class="text-white text-sm">info@at-salary.nl</p>
                </div>
                <div class="text-center">
                  <i class="pi pi-phone text-[#d6af84] text-lg mb-2 block"></i>
                  <p class="text-gray-400 text-sm">Phone</p>
                  <p class="text-white text-sm">+31 621309436</p>
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
import { ref, reactive } from "vue";
import Button from "primevue/button";
import Navbar from "../layouts/navbar.vue";
import Footer from "../layouts/footer.vue";

useHead({
  title: "Contact — @Salary",
  meta: [{ name: "description", content: "Contact page" }],
});

const isSubmitting = ref(false);

const form = reactive({
  name: "",
  email: "",
  subject: "",
  message: "",
});

const handleSubmit = async () => {
  isSubmitting.value = true;

  try {
    // Simulate API call
    await new Promise((resolve) => setTimeout(resolve, 1000));

    // Here you would typically send the form data to your API
    console.log("Form submitted:", form);

    // Reset form
    Object.assign(form, {
      name: "",
      email: "",
      subject: "",
      message: "",
    });

    // Show success message (you can use your preferred notification system)
    alert("Thank you for your message! We'll get back to you soon.");
  } catch (error) {
    console.error("Error submitting form:", error);
    alert("Sorry, there was an error sending your message. Please try again.");
  } finally {
    isSubmitting.value = false;
  }
};
</script>
