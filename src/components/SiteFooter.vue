<script setup lang="ts">
const year = new Date().getFullYear()
</script>

<template>
  <footer class="border-t border-slate-200 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
      <div class="grid md:grid-cols-4 gap-8 text-sm">
        <!-- Brand + Locations -->
        <div class="md:col-span-2">
          <div class="flex items-center gap-2">
            <div
              class="w-8 h-8 rounded-lg bg-emerald-600 grid place-items-center text-white font-semibold shadow-soft"
            >
              T
            </div>
            <span class="font-semibold tracking-tight">TradeCo Imports</span>
          </div>
          <p class="mt-3 text-slate-600">Rotterdam • Dubai • Lagos</p>
          <p class="mt-1 text-slate-600">
            © {{ year }} TradeCo B.V. All rights reserved.
          </p>
        </div>

        <!-- Company Links -->
        <div>
          <p class="font-semibold text-slate-800">Company</p>
          <ul class="mt-2 space-y-2 text-slate-600">
            <li><a href="#about" class="hover:text-emerald-600">About</a></li>
            <li><a href="#quality" class="hover:text-emerald-600">Quality</a></li>
            <li><a href="#logistics" class="hover:text-emerald-600">Logistics</a></li>
          </ul>
        </div>

        <!-- Contact Links -->
        <div>
          <p class="font-semibold text-slate-800">Contact</p>
          <ul class="mt-2 space-y-2 text-slate-600">
            <li>
              <a href="mailto:sales@tradeco.example" class="hover:text-emerald-600"
                >sales@tradeco.example</a
              >
            </li>
            <li>
              <a href="tel:+31101234567" class="hover:text-emerald-600">+31 10 123 4567</a>
            </li>
            <li>VAT: NL000000000B01</li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>
