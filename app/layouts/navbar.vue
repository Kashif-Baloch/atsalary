<template>
  <div class="bg-surface-900 py-4 shadow fixed top-0 left-0 w-full z-50">
    <div
      class="container mx-auto max-w-7xl px-4 flex items-center justify-between"
    >
      <div class="flex items-center gap-4 py-2">
        <RouterLink to="/">
          <img class="w-28" src="/archief/logo.svg" alt="logo" />
        </RouterLink>
      </div>
      <a
        v-styleclass="{
          selector: '@next',
          enterFromClass: 'hidden',
          leaveToClass: 'hidden',
          hideOnOutsideClick: true,
        }"
        class="cursor-pointer block lg:hidden text-surface-100 mt-1"
      >
        <i class="pi pi-bars text-2xl!" />
      </a>
      <div
        class="items-center grow justify-between hidden lg:flex absolute lg:static w-full left-0 top-full px-12 lg:px-0 z-50 shadow lg:shadow-none bg-surface-900"
      >
        <ul
          class="list-none p-0 py-4 lg:py-0 m-0 flex grow lg:items-center lg:justify-center text-surface-500 select-none flex-col lg:flex-row cursor-pointer"
        >
          <li class="">
            <RouterLink to="/product">
              <a
                v-styleclass="{
                  selector: '@next',
                  enterFromClass: 'hidden',
                  enterActiveClass: 'animate-scalein',
                  leaveToClass: 'hidden',
                  leaveActiveClass: 'animate-fadeout',
                  hideOnOutsideClick: true,
                }"
                class="flex px-0 text-white lg:px-8 py-4 items-center hover:text-blue-700 font-medium transition-colors duration-150 cursor-pointer"
              >
                <span>Producten</span>
              </a>
            </RouterLink>
          </li>
          <li>
            <RouterLink to="/about">
              <a
                class="flex px-0 lg:px-8 py-4 hover:text-blue-700 font-medium transition-colors text-white duration-150 cursor-pointer"
              >
                <span>Over ons</span>
              </a>
            </RouterLink>
          </li>
          <li>
            <RouterLink to="/price">
              <a
                class="flex px-0 lg:px-8 py-4 hover:text-blue-700 font-medium transition-colors text-white duration-150 cursor-pointer"
              >
                <span>Prijzen</span>
              </a>
            </RouterLink>
          </li>
          <li>
            <RouterLink to="/contact">
              <a
                class="flex px-0 lg:px-8 py-4 hover:text-blue-700 font-medium transition-colors text-white duration-150 cursor-pointer"
              >
                <span>Contact</span>
              </a>
            </RouterLink>
          </li>
        </ul>
        <div
          class="flex border-t lg:border-t-0 border-surface-700 lg:border-surface-800 py-4 lg:py-0 mt-4 lg:mt-0 gap-4"
        >
          <!-- <Button
          class="!text-white !bg-blue-700 !border-none !outline-none"
          label="Login"
        /> -->
          <Button
            class="!text-white !rounded-full !bg-blue-700 !border-none !outline-none"
            label="Naar portaal"
          />
        </div>
      </div>
    </div>
  </div>
</template>
