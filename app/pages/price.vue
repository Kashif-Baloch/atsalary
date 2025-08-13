<template>
  <Navbar />
  <div class="bg-surface-900 mt-20 p-12 lg:p-20">
    <div class="flex flex-wrap lg:flex-row flex-col-reverse gap-12">
      <div class="flex-1 p-4">
        <h1 class="text-5xl font-bold text-white mb-4 leading-tight">
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
          class="bg-gray-800 rounded-2xl p-8 max-w-md lg:max-w-xl mx-auto shadow-2xl border-2 border-blue-700"
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
                <a
                  href="#"
                  class="text-blue-700 hover:text-blue-600 text-sm transition-colors"
                >
                  <i class="pi pi-phone mr-1"></i>Call Sales
                </a>
                <a
                  href="#"
                  class="text-blue-700 hover:text-blue-600 text-sm transition-colors"
                >
                  <i class="pi pi-envelope mr-1"></i>Email Us
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="bg-surface-0 dark:bg-surface-950 p-6 md:p-12 lg:p-20">
    <div class="flex justify-center">
      <div class="flex flex-1">
        <div class="flex flex-1 flex-col">
          <div class="flex flex-col">
            <div
              class="flex flex-col gap-4 p-px pr-0 h-28 md:h-[146px] relative rounded-tl-xl z-10 before:content-[''] before:absolute before:inset-0 before:pointer-events-none before:bg-linear-to-b before:from-blue-500 dark:before:from-blue-400 before:to-transparent before:border-0 before:p-px before:rounded-tl-xl before:z-0"
            >
              <div
                class="relative z-10 h-full w-full bg-surface-0 dark:bg-surface-950 p-8 rounded-tl-xl"
              >
                <div
                  class="text-xl md:text-3xl leading-normal text-surface-900 dark:text-surface-0"
                >
                  Pricing
                </div>
                <div
                  class="text-sm leading-normal text-surface-500 dark:text-surface-400 md:flex hidden"
                >
                  Fringilla est ullamcorper eget nulla facilisi etiam
                </div>
              </div>
            </div>
            <div class="flex flex-col">
              <div
                v-for="feature in features"
                :key="feature"
                class="h-[42px] flex items-center border-b border-surface-100 dark:border-surface-800"
              >
                <div
                  class="px-8 text-sm font-medium text-surface-900 dark:text-surface-0"
                >
                  {{ feature }}
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="flex flex-1 flex-col">
          <div
            class="flex flex-col gap-4 p-px pr-0 pl-0 h-28 md:h-[146px] relative z-10 before:content-[''] before:absolute before:inset-0 before:pointer-events-none before:bg-linear-to-b before:from-blue-500 dark:before:from-blue-400 before:to-transparent before:border-0 before:p-px before:z-0"
          >
            <div
              class="relative z-10 h-full w-full bg-surface-0 dark:bg-surface-950 p-4 flex flex-col items-center gap-4"
            >
              <div class="flex flex-col gap-2">
                <div
                  class="text-lg md:text-xl leading-normal font-medium text-surface-900 dark:text-surface-0"
                >
                  Basic
                </div>
                <div
                  class="text-2xl md:text-3xl leading-normal font-medium text-surface-900 dark:text-surface-0 text-center"
                >
                  $10
                </div>
              </div>
              <Button
                type="button"
                rounded
                label="Free Trial"
                class="md:flex! !text-white hidden! !bg-blue-700 !border-none !outline-none"
              />
            </div>
          </div>
          <div class="flex flex-col">
            <div
              v-for="(value, index) in basicFeatures"
              :key="index"
              class="h-[42px] flex justify-center items-center border-b border-surface-100 dark:border-surface-800"
            >
              <i
                v-if="typeof value === 'boolean'"
                :class="[
                  'pi',
                  value
                    ? 'pi-check text-blue-500 dark:text-blue-400'
                    : 'pi-times text-surface-500 dark:text-surface-300',
                ]"
              />
              <div
                v-else
                class="text-sm text-surface-600 dark:text-surface-200"
              >
                Up to
                <span
                  class="text-surface-900 dark:text-surface-0 font-medium"
                  >{{ value }}</span
                >
                files
              </div>
            </div>
          </div>
        </div>

        <div class="flex flex-1 flex-col">
          <div
            class="flex flex-col gap-4 p-px pr-0 pl-0 h-28 md:h-[146px] relative z-10 before:content-[''] before:absolute before:inset-0 before:pointer-events-none before:bg-linear-to-b before:from-blue-500 dark:before:from-blue-400 before:to-transparent before:border-0 before:p-px before:z-0"
          >
            <div
              class="relative z-10 h-full w-full bg-surface-0 dark:bg-surface-950 p-4 flex flex-col items-center gap-4"
            >
              <div class="flex flex-col gap-2">
                <div
                  class="text-lg md:text-xl leading-normal font-medium text-surface-900 dark:text-surface-0"
                >
                  Premium
                </div>
                <div
                  class="text-2xl md:text-3xl leading-normal font-medium text-surface-900 dark:text-surface-0 text-center"
                >
                  $20
                </div>
              </div>
              <Button
                type="button"
                rounded
                label="Buy Now"
                class="md:flex! !text-white hidden! !bg-blue-700 !border-none !outline-none"
              />
            </div>
          </div>
          <div class="flex flex-col">
            <div
              v-for="(value, index) in premiumFeatures"
              :key="index"
              class="h-[42px] flex justify-center items-center border-b border-surface-100 dark:border-surface-800"
            >
              <i
                v-if="typeof value === 'boolean'"
                :class="[
                  'pi',
                  value
                    ? 'pi-check text-blue-500 dark:text-blue-400'
                    : 'pi-times text-surface-500 dark:text-surface-300',
                ]"
              />
              <div
                v-else
                class="text-sm text-surface-600 dark:text-surface-200"
              >
                Up to
                <span
                  class="text-surface-900 dark:text-surface-0 font-medium"
                  >{{ value }}</span
                >
                files
              </div>
            </div>
          </div>
        </div>

        <div class="flex flex-1 flex-col">
          <div
            class="flex flex-col gap-4 p-px pl-0 h-28 md:h-[146px] relative z-10 rounded-tr-xl before:content-[''] before:absolute before:inset-0 before:pointer-events-none before:bg-linear-to-b before:from-blue-500 dark:before:from-blue-400 before:to-transparent before:border-0 before:p-px before:rounded-tr-xl before:z-0"
          >
            <div
              class="relative z-10 h-full w-full bg-surface-0 dark:bg-surface-950 p-4 flex flex-col items-center gap-4 rounded-tr-xl"
            >
              <div class="flex flex-col gap-2">
                <div
                  class="text-lg md:text-xl leading-normal font-medium text-surface-900 dark:text-surface-0"
                >
                  Enterprise
                </div>
                <div
                  class="text-2xl md:text-3xl leading-normal font-medium text-surface-900 dark:text-surface-0 text-center"
                >
                  $30
                </div>
              </div>
              <Button
                type="button"
                rounded
                outlined
                label="Contact Us"
                class="md:flex! hidden! !text-blue-700 !border-blue-700"
              />
            </div>
          </div>
          <div class="flex flex-col">
            <div
              v-for="(value, index) in enterpriseFeatures"
              :key="index"
              class="h-[42px] flex justify-center items-center border-b border-surface-100 dark:border-surface-800"
            >
              <i
                v-if="typeof value === 'boolean'"
                :class="[
                  'pi',
                  value
                    ? 'pi-check text-blue-500 dark:text-blue-400'
                    : 'pi-times text-surface-500 dark:text-surface-300',
                ]"
              />
              <div
                v-else
                class="text-surface-900 dark:text-surface-0 text-sm font-medium"
              >
                {{ value }}
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
</script>
