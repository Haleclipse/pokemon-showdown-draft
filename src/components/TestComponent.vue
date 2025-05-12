<script setup lang="ts">
import { PlusIcon, MinusIcon } from 'lucide-vue-next'

const testStore = useTestStore()
const { increment, decrement } = testStore
const { count, name } = storeToRefs(testStore)
</script>

<template>
  <div>
    <!-- Counter Component -->
    <div class="text-center">
      <div>
        <div class="text-lg font-semibold mb-4">Name: {{ name }}</div>
        <Input
          v-model="name"
          type="text"
          class="max-w-xs mx-auto"
        />
      </div>
      <br />
      <div class="text-lg font-semibold mb-4">Count: {{ count }}</div>
      <div class="flex gap-2 justify-center">
        <Button
          variant="outline"
          @click="decrement"
        >
          <MinusIcon class="h-4 w-4 mr-2" />
          Decrement
        </Button>
        <Button
          @click="increment"
        >
          <PlusIcon class="h-4 w-4 mr-2" />
          Increment
        </Button>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
