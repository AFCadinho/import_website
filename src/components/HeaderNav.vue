<script setup lang="ts">
import { ref } from 'vue'

const open = ref(false)

const links = [
  { href: '#products', label: 'Products' },
  { href: '#about', label: 'About' },
  { href: '#quality', label: 'Quality' },
  { href: '#logistics', label: 'Logistics' },
  { href: '#contact', label: 'Contact' },
]
</script>

<template>
  <header class="sticky top-0 z-30 bg-white/90 backdrop-blur border-b border-slate-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <!-- Logo -->
        <a href="#home" class="flex items-center gap-2">
          <div class="w-9 h-9 rounded-xl bg-emerald-600 grid place-items-center text-white font-semibold shadow-md">
            T
          </div>
          <span class="font-semibold tracking-tight text-slate-900">TradeCo Imports</span>
        </a>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center gap-8 text-sm text-slate-700">
          <a v-for="l in links" :key="l.href" :href="l.href"
            class="hover:text-emerald-600 transition-colors duration-200">
            {{ l.label }}
          </a>
        </nav>

        <!-- CTA Button -->
        <a href="#contact"
          class="hidden sm:inline-flex items-center gap-2 px-4 py-2 rounded-xl bg-emerald-600 text-white hover:bg-emerald-700 shadow-md transition-all duration-200">
          Get a Quote
        </a>

        <!-- Mobile Menu Button -->
        <button class="md:hidden p-2 text-slate-700 hover:text-emerald-600 transition-colors duration-200"
          @click="open = !open" aria-label="Menu">
          ☰
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-if="open" class="md:hidden border-t border-slate-200 bg-white">
      <nav class="px-4 py-3 space-y-2 text-slate-700">
        <a v-for="l in links" :key="l.href" :href="l.href" @click="open = false"
          class="block py-2 hover:text-emerald-600 transition-colors duration-200">
          {{ l.label }}
        </a>
      </nav>
    </div>
  </header>
</template>
