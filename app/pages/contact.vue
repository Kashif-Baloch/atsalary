<template>
  <Navbar />

  <div class="bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 mt-20 py-12 lg:py-20">
      <div class="flex flex-wrap lg:flex-row flex-col gap-12">
        <div class="flex-1 md:p-4">
          <h1
            class="lg:text-5xl text-3xl font-bold text-white mb-4 leading-tight"
          >
            Get in touch with us
            <span class="text-blue-700 underline">today</span>
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            We'd love to hear from you. Send us a message and we'll respond as
            soon as possible.
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-phone text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Quick response within 24 hours.</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-envelope text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Professional support team ready to help.</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-users text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Personalized solutions for your business needs.</span
              >
            </li>
          </ul>
        </div>

        <div class="flex-1 md:p-4 text-left">
          <div
            class="bg-blue-50/50 dark:bg-blue-400/10 rounded-2xl md:p-8 p-4 py-8 md:py-8 lg:max-w-xl mx-auto shadow-2xl"
          >
            <h2 class="text-2xl font-bold text-white mb-6">Contact Form</h2>
            <form @submit.prevent="handleSubmit" class="space-y-6">
              <div>
                <label
                  class="block text-gray-400 text-sm font-medium mb-2"
                  for="name"
                >
                  Full Name
                </label>
                <input
                  v-model="form.name"
                  type="text"
                  id="name"
                  name="name"
                  required
                  class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:border-transparent transition-all"
                  placeholder="Enter your full name"
                />
              </div>

              <div>
                <label
                  class="block text-gray-400 text-sm font-medium mb-2"
                  for="email"
                >
                  Email Address
                </label>
                <input
                  v-model="form.email"
                  type="email"
                  id="email"
                  name="email"
                  required
                  class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:border-transparent transition-all"
                  placeholder="Enter your email address"
                />
              </div>

              <div>
                <label
                  class="block text-gray-400 text-sm font-medium mb-2"
                  for="message"
                >
                  Message
                </label>
                <textarea
                  v-model="form.message"
                  id="message"
                  name="message"
                  rows="4"
                  required
                  class="w-full px-4 py-3 bg-gray-700 border border-gray-600 rounded-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-700 focus:border-transparent transition-all resize-none"
                  placeholder="Tell us more about your inquiry..."
                ></textarea>
              </div>

              <Button
                type="submit"
                :loading="isSubmitting"
                label="Send Message"
                rounded
                size="large"
                class="w-full !text-white !bg-blue-700 !border-none !outline-none"
              />
            </form>

            <div class="mt-8 pt-6 border-t border-gray-700">
              <div class="flex justify-center gap-4">
                <div class="text-center">
                  <i class="pi pi-envelope text-primary text-lg mb-2 block"></i>
                  <p class="text-gray-400 text-sm">Email</p>
                  <p class="text-white text-sm">hello@company.com</p>
                </div>
                <div class="text-center">
                  <i class="pi pi-phone text-primary text-lg mb-2 block"></i>
                  <p class="text-gray-400 text-sm">Phone</p>
                  <p class="text-white text-sm">+1 (555) 123-4567</p>
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

const features = [
  "Arcu purus",
  "Posuere felis",
  "Curabitur mollis",
  "Vitae odio",
  "Orci, mi",
  "Tincidunt vulputate",
  "Quis felis",
  "Dignissim vivamus",
];

const basicFeatures = [true, true, true, true, false, false, false, "5"];
const premiumFeatures = [true, true, true, true, true, false, false, "10"];
const enterpriseFeatures = [
  true,
  true,
  true,
  true,
  true,
  true,
  true,
  "Unlimited",
];
const stats = ref([
  {
    icon: "pi pi-video",
    value: "52000",
    label: "Streams",
  },
  {
    icon: "pi pi-heart",
    value: "21000",
    label: "Engagement",
  },
  {
    icon: "pi pi-clock",
    value: "71.2",
    label: "Watch Time",
  },
  {
    icon: "pi pi-thumbs-up",
    value: "4500",
    label: "Likes",
  },
]);
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
