<template>
  <div class="bg-surface-0 dark:bg-surface-900">
    <div class="container mx-auto max-w-7xl px-4 py-20 flex flex-col gap-8">
      <!-- <div class="h-px bg-surface-300 dark:bg-surface-700" /> -->
      <!-- <div
        class="grid xl:grid-cols-6 md:grid-cols-3 grid-cols-1 sm:grid-cols-2 gap-8"
      >
        <div class="flex flex-col gap-6">
          <div
            class="text-surface-900 dark:text-surface-0 font-bold leading-tight"
          >
            Company
          </div>
          <div class="flex flex-col gap-4">
            <a
              v-for="item in [
                'About Us',
                'News',
                'Investor Relations',
                'Careers',
                'Media Kit',
              ]"
              :key="item"
              class="text-surface-700 dark:text-surface-400 hover:text-surface-900 dark:hover:text-surface-0 leading-tight transition-colors cursor-pointer"
            >
              {{ item }}
            </a>
          </div>
        </div>
        <div class="flex flex-col gap-6">
          <div
            class="text-surface-900 dark:text-surface-0 font-bold leading-tight"
          >
            Resources
          </div>
          <div class="flex flex-col gap-4">
            <a
              v-for="item in ['Get Started', 'Learn', 'Case Studies']"
              :key="item"
              class="text-surface-700 dark:text-surface-400 hover:text-surface-900 dark:hover:text-surface-0 leading-tight transition-colors cursor-pointer"
            >
              {{ item }}
            </a>
          </div>
        </div>
        <div class="flex flex-col gap-6">
          <div
            class="text-surface-900 dark:text-surface-0 font-bold leading-tight"
          >
            Developer
          </div>
          <div class="flex flex-col gap-4">
            <a
              v-for="item in [
                'Courses',
                'Documentation',
                'API Reference',
                'Status',
                'Papers',
                'Development Blog',
              ]"
              :key="item"
              class="text-surface-700 dark:text-surface-400 hover:text-surface-900 dark:hover:text-surface-0 leading-tight transition-colors cursor-pointer"
            >
              {{ item }}
            </a>
          </div>
        </div>
        <div class="flex flex-col gap-6">
          <div
            class="text-surface-900 dark:text-surface-0 font-bold leading-tight"
          >
            Community
          </div>
          <div class="flex flex-col gap-4">
            <a
              v-for="item in ['Discord', 'Events', 'FAQ', 'Blog']"
              :key="item"
              class="text-surface-700 dark:text-surface-400 hover:text-surface-900 dark:hover:text-surface-0 leading-tight transition-colors cursor-pointer"
            >
              {{ item }}
            </a>
          </div>
        </div>
        <div class="flex flex-col gap-6">
          <div
            class="text-surface-900 dark:text-surface-0 font-bold leading-tight"
          >
            Connect
          </div>
          <div class="flex flex-col gap-4">
            <a
              v-for="item in [
                'Newsletters',
                'Press',
                'Code of Conduct',
                'Security Guide',
                'Bug Bounty Program',
              ]"
              :key="item"
              class="text-surface-700 dark:text-surface-400 hover:text-surface-900 dark:hover:text-surface-0 leading-tight transition-colors cursor-pointer"
            >
              {{ item }}
            </a>
          </div>
        </div>
        <div class="flex flex-col gap-6">
          <div
            class="text-surface-900 dark:text-surface-0 font-bold leading-tight"
          >
            Legal
          </div>
          <div class="flex flex-col gap-4">
            <a
              v-for="item in [
                'Brand Policy',
                'Privacy Policy',
                'Terms of Service',
              ]"
              :key="item"
              class="text-surface-700 dark:text-surface-400 hover:text-surface-900 dark:hover:text-surface-0 leading-tight transition-colors cursor-pointer"
            >
              {{ item }}
            </a>
          </div>
        </div>
      </div> -->
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
