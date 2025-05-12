<script setup lang="ts">
import { Button } from '@/components/ui/button'
</script>

<template>
  <div class="prose dark:prose-invert max-w-none">
    <RouterLinkUp />

    <h1>About Us</h1>

    <p>
      Welcome to our platform! We are dedicated to providing the best service to
      our users. Our mission is to deliver high-quality products and exceptional
      customer support.
    </p>

    <p>Thank you for choosing us. We look forward to serving you!</p>

    <div class="flex flex-wrap gap-2 mt-6">
      <RouterLink to="/common/change-log">
        <Button variant="outline" size="sm">Change Log</Button>
      </RouterLink>

      <RouterLink to="/common/help">
        <Button variant="outline" size="sm">Help</Button>
      </RouterLink>

      <RouterLink to="/common/privacy-policy">
        <Button variant="outline" size="sm">Privacy Policy</Button>
      </RouterLink>

      <RouterLink to="/common/terms-of-service">
        <Button variant="outline" size="sm">Terms</Button>
      </RouterLink>
    </div>
  </div>
</template>
