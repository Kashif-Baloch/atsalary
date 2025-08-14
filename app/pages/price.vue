<template>
  <Navbar />

  <div class="bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 mt-20 py-12 lg:py-20">
      <div class="flex flex-wrap lg:flex-row flex-col-reverse gap-12">
        <div class="flex-1 md:p-4">
          <h1
            class="lg:text-5xl text-3xl font-bold text-white mb-4 leading-tight"
          >
            Simple pricing that grows with you
            <span class="text-blue-700 underline">€30,00</span>
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            Everything you need to manage your social CRM and grow your business
            in one affordable package.
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-check text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Unlimited contacts and social profiles management.</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-check text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >Advanced analytics and reporting tools.</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-check text-primary text-xl!" />
              <span class="text-gray-400 leading-normal"
                >24/7 customer support and priority assistance.</span
              >
            </li>
          </ul>
          <Button
            label="Get Started Now"
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
                Only Package Available
              </div>
              <h2 class="text-3xl font-bold text-white mb-2">
                Complete CRM Package
              </h2>
              <div class="flex items-center justify-center gap-2">
                <span class="text-5xl font-bold text-blue-700">€30,00</span>
                <span class="text-gray-400 text-lg">/month</span>
              </div>
            </div>

            <div class="space-y-6 mb-8">
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Unlimited Social Accounts</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Advanced CRM Features</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Real-time Analytics</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Automated Workflows</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">Priority Support</span>
              </div>
              <div class="flex items-center gap-3">
                <i class="pi pi-check-circle text-primary text-lg"></i>
                <span class="text-gray-300">API Access</span>
              </div>
            </div>

            <Button
              label="Choose This Plan"
              rounded
              size="large"
              class="w-full !text-white !bg-blue-700 !border-none !outline-none mb-4"
              @click="handleChoosePlan"
            />

            <div class="text-center">
              <p class="text-gray-400 text-sm">
                <i class="pi pi-shield-check text-primary mr-2"></i>
                30-day money-back guarantee
              </p>
            </div>

            <div class="mt-6 pt-6 border-t border-gray-700">
              <div class="text-center">
                <p class="text-gray-400 text-sm mb-2">Need help choosing?</p>
                <div class="flex justify-center space-x-4">
                  <a href="#" class="text-gray-400 text-sm transition-colors">
                    <i class="pi pi-phone mr-1 text-[#d6af84]"></i>Call Sales
                  </a>
                  <a href="#" class="text-gray-400 text-sm transition-colors">
                    <i class="pi pi-envelope mr-1 text-[#d6af84]"></i>Email Us
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
