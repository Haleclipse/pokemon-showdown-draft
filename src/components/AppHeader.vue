<script setup lang="ts">
import { HelpCircle, Settings } from 'lucide-vue-next'
</script>

<template>
  <div class="flex justify-between gap-4 p-2 bg-neutral">
    <RouterLink
      to="/"
      class="flex gap-2 items-center"
    >
      <img
        src="@assets/logo.png"
        alt="logo"
        class="h-8 w-auto"
      />
      <div class="font-semibold text-primary">
        Vite Vue 3 Chrome Extension
      </div>
    </RouterLink>
    <div class="flex gap-2 justify-center">
      <RouterLink to="/common/about">
        <Button variant="ghost" size="icon">
          <HelpCircle class="h-4 w-4" />
        </Button>
      </RouterLink>
      <RouterLink to="/options-page">
        <Button variant="ghost" size="icon">
          <Settings class="h-4 w-4" />
        </Button>
      </RouterLink>
      <ThemeSwitch />
    </div>
  </div>
</template>

<style scoped></style>
