<script setup lang="ts">
defineProps<{
  title: string
  image: string
  points: string[]
}>()
</script>

<template>
  <article
    class="rounded-2xl border border-slate-200 bg-white p-6 shadow-md hover:shadow-lg transition-shadow duration-200"
  >
    <div class="aspect-16/10 rounded-xl overflow-hidden bg-slate-100">
      <img :src="image" :alt="title" class="w-full h-full object-cover" />
    </div>

    <h3 class="mt-4 text-lg font-semibold text-slate-900">{{ title }}</h3>
    <ul class="mt-2 text-sm text-slate-600 space-y-1 list-disc pl-5">
      <li v-for="(p, i) in points" :key="i">{{ p }}</li>
    </ul>
  </article>
</template>
