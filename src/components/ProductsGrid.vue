<script setup lang="ts">
import ProductCard from './ProductCard.vue'

const products = [
  {
    title: 'Rice',
    image: 'https://images.unsplash.com/photo-1604908554049-4f0b1fc01019?w=1200&q=80',
    points: ['5%–25% Broken White Rice', 'Parboiled 100% Sortex', 'Basmati & Jasmine on request'],
  },
  {
    title: 'Refined Palm Oil',
    image: 'https://images.unsplash.com/photo-1506619216599-9d16d0903dfd?w=1200&q=80',
    points: ['RBD Palm Olein CP8 / CP10', 'Jerrycans, drums, flexi-tanks', 'Private label options'],
  },
  {
    title: 'Other Commodities',
    image: 'https://images.unsplash.com/photo-1515003197210-e0cd71810b5f?w=1200&q=80',
    points: ['Sugar ICUMSA 45/150', 'Sunflower / Soybean Oil', 'Wheat Flour & pulses'],
  },
]
</script>

<template>
  <section id="products" class="py-16 lg:py-24">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Header -->
      <div class="flex items-end justify-between gap-6 mb-10">
        <div>
          <h2 class="text-3xl sm:text-4xl font-bold tracking-tight">Core Products</h2>
          <p class="mt-2 text-slate-600">
            Popular specifications held in stock and available on contract.
          </p>
        </div>

        <!-- CTA Button -->
        <a href="#contact" class="hidden sm:inline-block px-4 py-2 rounded-xl border border-slate-300 text-slate-700
                 hover:border-emerald-600 hover:text-emerald-600 transition-colors duration-200">
          Request a full catalogue
        </a>
      </div>

      <!-- Product Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
        <ProductCard v-for="p in products" :key="p.title" v-bind="p" />
      </div>
    </div>
  </section>
</template>
