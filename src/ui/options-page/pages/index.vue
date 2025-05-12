<script setup lang="ts">
import { Input } from '@/components/ui/input'
import { Switch } from '@/components/ui/switch'
import { Label } from '@/components/ui/label'
import {
  Form,
  FormControl,
  FormDescription,
  FormField,
  FormItem,
  FormLabel,
  FormMessage
} from '@/components/ui/form'

const optionsStore = useOptionsStore()
const { isDark, profile, others } = storeToRefs(optionsStore)
</script>

<template>
  <div
    class="max-w-xl w-full mx-auto rounded-xl md:my-12 p-4 md:p-8 md:border border-border md:shadow-lg bg-background"
  >
    <RouterLinkUp />

    <h1>Options</h1>
    <p>
      You can configure various options related to this extension here. These
      options/ settings are peristent, available in all contexts, implemented
      using Pinia and useBrowserStorage composable.
    </p>

    <h3 class="mt-6 mb-2 text-lg font-semibold">User Interface</h3>
    <p>Change application interface settings.</p>

    <div class="space-y-6 mt-4">
      <div class="flex items-center justify-between space-x-2">
        <Label for="theme" class="flex flex-col space-y-1">
          <span>Theme</span>
        </Label>
        <Switch id="theme" v-model="isDark" />
      </div>

      <div>
        <h3 class="mt-6 mb-2 text-lg font-semibold">Profile</h3>
        <p>Change your name and age.</p>
      </div>

      <div class="space-y-4">
        <div class="space-y-2">
          <Label for="name">Name</Label>
          <Input id="name" v-model="profile.name" />
        </div>

        <div class="space-y-2">
          <Label for="age">Age</Label>
          <Input id="age" v-model="profile.age" />
        </div>
      </div>

      <div>
        <h3 class="mt-6 mb-2 text-lg font-semibold">Others</h3>
        <p>Some other settings related to extension usage.</p>
      </div>

      <div class="flex items-center justify-between space-x-2">
        <Label for="awesome" class="flex flex-col space-y-1">
          <span>Awesome Feature</span>
        </Label>
        <Switch id="awesome" v-model="others.awesome" />
      </div>

      <div class="space-y-2">
        <Label for="counter">Counter</Label>
        <Input id="counter" v-model="others.counter" type="number" />
      </div>

      <p class="text-sm text-muted-foreground mt-6">
        * You can also make this a component and then able to use this in any
        context like Popup, Developer Tools UI etc
      </p>
      <p class="text-sm text-muted-foreground">Feel free to change groups or options as per your requirements.</p>
    </div>
  </div>
</template>
