<template>
  <div class="welcome">
    <scroll-indicator />
    <v-container>
      <the-nav-bar />
      <v-main>
        <hero-section />
        <about-us-section />
        <our-values-section />
        <our-projects-section />
        <our-services-section />
        <our-vision-section />
      </v-main>
      <scroll-to-top />
    </v-container>
  </div>
</template>

<script>
  export default {
    name: 'welcome',
    components: {
      TheNavBar: () => import('@/components/layouts/TheNavBar'),
      HeroSection: () => import('@/components/sections/HeroSection'),
      AboutUsSection: () => import('@/components/sections/AboutUsSection'),
      OurValuesSection: () => import('@/components/sections/OurValuesSection'),
      OurProjectsSection: () => import('@/components/sections/OurProjectsSection'),
      OurServicesSection: () => import('@/components/sections/OurServicesSection'),
      OurVisionSection: () => import('@/components/sections/OurVisionSection'),
      ScrollToTop: () => import('@/components/sections/ScrollToTop'),
      ScrollIndicator: () => import('@/components/sections/ScrollIndicator')
    }
  }
</script>