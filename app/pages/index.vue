<template>
  <Navbar />

  <div class="bg-surface-900 mt-20 py-12 lg:py-20">
    <div class="container mx-auto max-w-7xl px-4">
      <div
        class="flex flex-wrap lg:flex-row flex-col-reverse gap-12 items-center"
      >
        <div class="flex-1 md:p-4">
          <h1
            class="text-2xl lg:text-5xl font-bold text-white mb-4 leading-tight"
          >
            Klonker gave pagina
            <span class="text-blue-700 underline">for free</span>
          </h1>
          <p class="text-2xl text-gray-400 mb-8 leading-normal">
            Arcu cursus euismod quis viverra nibh cras. Amet justo donec enim
            diam vulputate ut.
          </p>
          <ul class="list-none flex flex-col gap-4">
            <li class="flex items-center gap-2">
              <i class="pi pi-trophy text-[#d6af84] text-xl!" /><span
                class="text-gray-400 leading-normal"
                >Senectus et netus et malesuada fames.</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-sparkles text-[#d6af84] text-xl!" /><span
                class="text-gray-400 leading-normal"
                >Orci a scelerisque purus semper eget.</span
              >
            </li>
            <li class="flex items-center gap-2">
              <i class="pi pi-bolt text-[#d6af84] text-xl!" /><span
                class="text-gray-400 leading-normal"
                >Aenean sed adipiscing diam donec adipiscing tristique.</span
              >
            </li>
          </ul>
          <RouterLink to="/contact">
            <Button
              label="Claim Your Account"
              rounded
              size="large"
              class="mt-12 !bg-blue-700 !border-none !text-white !outline-none"
            />
          </RouterLink>
        </div>
        <div class="flex-1 text-center lg:text-right overflow-hidden">
          <img
            src="/archief/pic1.png"
            alt="Image"
            class="w-full max-w-md lg:w-auto lg:max-w-xl mx-auto"
          />
        </div>
      </div>
    </div>
  </div>

  <Footer />
</template>
<script setup>
import Button from "primevue/button";
import Navbar from "../layouts/navbar.vue";
import Footer from "../layouts/footer.vue";
</script>
<style>
@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-marquee {
  animation: marquee 30s linear infinite;
}
</style>
