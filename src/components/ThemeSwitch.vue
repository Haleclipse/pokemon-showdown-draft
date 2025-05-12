<script lang="ts" setup>
import { Button } from '@/components/ui/button'
import { SunIcon, MoonIcon } from 'lucide-vue-next'

const { isDark, toggleDark } = useTheme()
applyTheme(isDark ? "dark" : "light")
</script>

<template>
  <Button
    variant="ghost"
    size="icon"
    @click="toggleDark"
  >
    <SunIcon v-if="!isDark" class="h-4 w-4" />
    <MoonIcon v-else class="h-4 w-4" />
  </Button>
</template>
