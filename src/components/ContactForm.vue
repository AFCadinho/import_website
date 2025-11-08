<script setup lang="ts">
import { ref, computed } from 'vue'

const form = ref({
  name: '',
  company: '',
  email: '',
  phone: '',
  spec: '',
  destination: '',
  incoterms: 'FOB',
})

const submitted = ref(false)
const valid = computed(
  () => form.value.name.trim() && form.value.email.trim() && form.value.spec.trim()
)

function submit() {
  if (!valid.value) return
  submitted.value = true
  // TODO: integrate EmailJS/Formspark/your API here
}
</script>

<template>
  <section id="contact" class="py-16">
    <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center max-w-2xl mx-auto">
        <h2 class="text-3xl sm:text-4xl font-bold tracking-tight text-slate-900">Request a Quote</h2>
        <p class="mt-2 text-slate-600">
          Tell us what you need — product, spec, packaging and destination — and we’ll reply with pricing and lead times.
        </p>
      </div>

      <form
        @submit.prevent="submit"
        class="mt-10 grid gap-4 bg-white rounded-2xl border border-slate-200 p-6 shadow-md"
        novalidate
      >
        <div class="grid sm:grid-cols-2 gap-4">
          <div>
            <label class="block text-sm font-medium text-slate-800" for="name">Name</label>
            <input
              id="name"
              v-model="form.name"
              name="name"
              type="text"
              placeholder="Your name"
              required
              autocomplete="name"
              class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                     focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
            />
          </div>
          <div>
            <label class="block text-sm font-medium text-slate-800" for="company">Company</label>
            <input
              id="company"
              v-model="form.company"
              name="company"
              type="text"
              placeholder="Company name"
              autocomplete="organization"
              class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                     focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
            />
          </div>
        </div>

        <div class="grid sm:grid-cols-2 gap-4">
          <div>
            <label class="block text-sm font-medium text-slate-800" for="email">Email</label>
            <input
              id="email"
              v-model="form.email"
              name="email"
              type="email"
              placeholder="you@company.com"
              required
              autocomplete="email"
              class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                     focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
            />
          </div>
          <div>
            <label class="block text-sm font-medium text-slate-800" for="phone">Phone</label>
            <input
              id="phone"
              v-model="form.phone"
              name="phone"
              type="tel"
              placeholder="+31 …"
              autocomplete="tel"
              class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                     focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
            />
          </div>
        </div>

        <div>
          <label class="block text-sm font-medium text-slate-800" for="spec">Product & Specification</label>
          <textarea
            id="spec"
            v-model="form.spec"
            name="spec"
            placeholder="e.g., Rice 5% broken, 50kg PP bags, CIF Rotterdam"
            rows="4"
            required
            class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                   focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
          ></textarea>
        </div>

        <div class="grid sm:grid-cols-2 gap-4">
          <div>
            <label class="block text-sm font-medium text-slate-800" for="destination">Destination</label>
            <input
              id="destination"
              v-model="form.destination"
              name="destination"
              type="text"
              placeholder="City, Country"
              class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                     focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
            />
          </div>
          <div>
            <label class="block text-sm font-medium text-slate-800" for="incoterms">Incoterms</label>
            <select
              id="incoterms"
              v-model="form.incoterms"
              name="incoterms"
              class="mt-1 w-full rounded-xl border border-slate-300 bg-white px-3 py-2
                     focus:outline-none focus:ring-2 focus:ring-emerald-500 focus:border-emerald-500"
            >
              <option>FOB</option>
              <option>CIF</option>
              <option>EXW</option>
              <option>DDP</option>
            </select>
          </div>
        </div>

        <div class="flex items-center justify-between">
          <p class="text-xs text-slate-500">
            By submitting, you agree to our <a href="#" class="underline">privacy policy</a>.
          </p>
          <button
            :disabled="!valid"
            type="submit"
            class="px-5 py-3 rounded-xl bg-emerald-600 text-white hover:bg-emerald-700
                   disabled:opacity-50 disabled:cursor-not-allowed shadow-md transition-colors duration-200"
          >
            Submit Request
          </button>
        </div>

        <p v-if="submitted" class="text-sm text-emerald-700 mt-2" aria-live="polite">
          Thanks! We'll get back to you via email.
        </p>
      </form>

      <div class="mt-6 text-center text-sm text-slate-600">
        Prefer WhatsApp?
        <a href="https://wa.me/31101234567" class="text-emerald-600 underline">Message us</a>
      </div>
    </div>
  </section>
</template>
