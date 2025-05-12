<script setup lang="ts">
import { ArrowLeftIcon } from 'lucide-vue-next'

const router = useRouter()

defineProps<{
  label?: string
}>()
</script>

<template>
  <Button
    class="my-4"
    variant="outline"
    @click="router.back()"
  >
    <ArrowLeftIcon class="h-4 w-4 mr-2" />
    {{ label || "Go Back" }}
  </Button>
</template>

<style scoped></style>
