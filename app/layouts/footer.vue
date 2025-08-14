<template>
  <div class="bg-surface-0 dark:bg-surface-900 pb-10">
    <div class="container mx-auto max-w-7xl px-4 py-4 flex flex-col gap-8">
      <div class="h-px bg-surface-300 dark:bg-surface-700" />
      <div class="flex flex-col sm:flex-row items-center justify-between gap-4">
        <span class="text-surface-500 dark:text-surface-400 leading-tight"
          >&copy; 2025 AtSalary all rights reserved</span
        >
        <div class="flex items-center gap-4">
          <a
            v-for="icon in ['twitter', 'github', 'slack']"
            :key="icon"
            class="cursor-pointer"
          >
            <i
              :class="`pi pi-${icon} text-lg text-surface-500 hover:text-surface-900 dark:text-surface-400 dark:hover:text-surface-0 transition-colors`"
            />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
