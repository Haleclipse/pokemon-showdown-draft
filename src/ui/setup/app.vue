<script setup lang="ts"></script>

<template>
  <div class="min-h-screen bg-background text-foreground">
    <AppHeader />

    <div class="w-full p-4 prose dark:prose-invert">
      <RouterView />
    </div>

    <AppFooter />
  </div>
</template>

<style lang="css"></style>
