<template>
  <div>
    <TopBar/>
    <HeaderNav />
    <HeroSection />
    <ProductsGrid
      title="Our Products"
      image="path/to/image.jpg"
      :points="['Point 1', 'Point 2', 'Point 3']"
    />
    <AboutBlock />
    <QualitySection />
    <LogisticsSection />
    <ContactForm />
    <SiteFooter />
  </div>
</template>

<script setup lang="ts">
import TopBar from '@/components/TopBar.vue';
import HeaderNav from '@/components/HeaderNav.vue'
import HeroSection from '@/components/HeroSection.vue'
import ProductsGrid from '@/components/ProductsGrid.vue';
import AboutBlock from '@/components/AboutBlock.vue'
import QualitySection from '@/components/QualitySection.vue'
import LogisticsSection from '@/components/LogisticsSection.vue'
import ContactForm from '@/components/ContactForm.vue'
import SiteFooter from '@/components/SiteFooter.vue'
</script>
