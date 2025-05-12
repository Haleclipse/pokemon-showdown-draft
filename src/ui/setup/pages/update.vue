<script setup lang="ts">
import { Button } from '@/components/ui/button'

const displayName = __DISPLAY_NAME__
const version = __VERSION__
</script>

<template>
  <div
    class="w-full h-full flex flex-col justify-center items-center text-center md:my-12 prose dark:prose-invert max-w-none"
  >
    <h1>🎉 Updated! 🚀</h1>
    <p class="text-xl">
      Thank you for installing {{ displayName }}! ❤️
      <br />
      Now you can close this tab and start using the extension.
    </p>

    <p class="text-lg">
      New Version: {{ version }}
      <br />
      <RouterLink to="/common/change-log" class="mt-2 inline-block">
        <Button>Change Log</Button>
      </RouterLink>
    </p>

    <hr class="w-full my-6" />

    <div class="flex flex-wrap gap-2 justify-center">
      <RouterLink
        v-for="route in appRouter.getRoutes()"
        :key="route.path"
        :to="route.path"
      >
        <Button variant="outline" size="sm">{{ route.path }}</Button>
      </RouterLink>
    </div>
  </div>
</template>
