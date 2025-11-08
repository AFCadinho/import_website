<template>
  <section id="home" class="relative overflow-hidden">
    <!-- Background gradient -->
    <div class="absolute inset-0 -z-10 bg-linear-to-b from-emerald-50 to-white"></div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-28">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Text content -->
        <div>
          <h1 class="text-4xl sm:text-5xl font-extrabold tracking-tight leading-tight text-slate-900">
            Importing
            <span class="text-emerald-600">Rice</span>,
            <span class="text-emerald-600">Palm Oil</span>
            & Essential Commodities
          </h1>
          <p class="mt-5 text-lg text-slate-600 max-w-prose">
            We source directly from vetted mills and producers for consistent
            quality, competitive pricing, and dependable delivery.
          </p>

          <!-- Buttons -->
          <div class="mt-8 flex flex-wrap gap-3">
            <a href="#products"
              class="px-5 py-3 rounded-xl bg-emerald-600 text-white hover:bg-emerald-700 shadow-md transition-all duration-200">Explore
              Products</a>
            <a href="#contact"
              class="px-5 py-3 rounded-xl border border-slate-300 text-slate-700 hover:border-emerald-600 hover:text-emerald-600 transition-colors duration-200">Request
              Pricing</a>
          </div>

          <!-- Social proof -->
          <div class="mt-8 flex items-center gap-6 text-sm text-slate-600">
            <div class="flex -space-x-2">
              <img class="w-8 h-8 rounded-full ring-2 ring-white"
                src="https://images.unsplash.com/photo-1544723795-3fb6469f5b39?w=80&q=80" alt="client" />
              <img class="w-8 h-8 rounded-full ring-2 ring-white"
                src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=80&q=80" alt="client" />
              <img class="w-8 h-8 rounded-full ring-2 ring-white"
                src="https://images.unsplash.com/photo-1502685104226-ee32379fefbe?w=80&q=80" alt="client" />
            </div>
            <span>100+ satisfied clients worldwide</span>
          </div>
        </div>

        <!-- Image + Badge -->
        <div class="relative">
          <div class="aspect-4/3 rounded-2xl overflow-hidden shadow-md bg-white">
            <img src="https://images.unsplash.com/photo-1590559899731-a382839e5549?w=1600&q=80"
              alt="Bags of rice in warehouse" class="w-full h-full object-cover" />
          </div>
          <div
            class="absolute -bottom-6 -left-6 bg-white/90 backdrop-blur border border-slate-200 rounded-2xl p-4 shadow-md hidden sm:block">
            <p class="text-sm font-medium text-slate-900">Origin Traceability</p>
            <p class="text-xs text-slate-600">
              Lot-level documentation for every shipment
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
