<template>
  <div class="relative dark:bg-slate-800">
    <div class="absolute inset-0 flex items-center" aria-hidden="true">
      <div class="w-full border-t border-gray-300 dark:border-slate-600" />
    </div>
    <div class="relative flex justify-center">
      <span class="bg-white dark:bg-slate-800 px-2 text-gray-500">
        <PlusIcon class="h-5 w-5 text-gray-500" aria-hidden="true" />
      </span>
    </div>
  </div>
</template>

<script setup>
import { PlusIcon } from "@heroicons/vue/20/solid";
</script>
