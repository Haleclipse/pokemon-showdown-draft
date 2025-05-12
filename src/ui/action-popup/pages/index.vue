<script setup lang="ts">
import { Button } from '@/components/ui/button'
import { HeartIcon, PresentationIcon, RocketIcon } from 'lucide-vue-next'
</script>

<template>
  <div>
    <div class="py-6">
      <div class="text-center">
        <div class="max-w-md mx-auto">
          <h1 class="text-2xl font-bold mb-2">Welcome!</h1>
          <p class="mb-6">
            Unlock productivity and streamline your workflow with our SaaS
            Chrome extension platform.
          </p>

          <div class="flex gap-2 justify-center mb-6">
            <RouterLink to="/common/features">
              <Button variant="outline">
                <HeartIcon class="h-4 w-4 mr-2" />
                Features
              </Button>
            </RouterLink>
            <RouterLink to="/common/pricing">
              <Button variant="outline">
                <PresentationIcon class="h-4 w-4 mr-2" />
                Pricing
              </Button>
            </RouterLink>
          </div>

          <RouterLink to="/common/account/login">
            <Button size="lg" class="w-full">
              <RocketIcon class="h-4 w-4 mr-2" />
              Get Started Now
            </Button>
          </RouterLink>

          <div class="flex justify-evenly my-6 text-sm">
            <RouterLink to="/action-popup/playground" class="text-primary hover:underline">
              Playground
            </RouterLink>

            <a href="https://github.com/mubaidr/vite-vue3-browser-extension-v3" class="text-primary hover:underline">
              Documentation
            </a>

            <a href="https://mubaidr.js.org" class="text-primary hover:underline">
              Support
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
