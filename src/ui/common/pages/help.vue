<script setup lang="ts">
</script>

<template>
  <div class="prose dark:prose-invert max-w-none">
    <RouterLinkUp />

    <h1>Help & Support</h1>
    <p>
      Need assistance? We are here to help! For any issues or questions, you can
      contact our support team at:
      <a
        href="mailto:support@example.com"
        class="text-primary hover:underline"
      >
        support@example.com
      </a>
    </p>

    <p class="text-muted-foreground">
      We strive to respond to all inquiries within 24 hours. Thank you for your
      patience and understanding.
    </p>

    <div class="flex flex-wrap gap-2 mt-6">
      <RouterLink to="/common/about">
        <Button variant="outline" size="sm">About Us</Button>
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
