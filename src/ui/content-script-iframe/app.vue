<script setup lang="ts"></script>

<template>
  <div class="min-h-screen bg-background text-foreground">
    <AppHeader />

    <div class="p-4 prose dark:prose-invert">
      <RouterView />
    </div>

    <AppFooter />
  </div>
</template>

<style scoped></style>
