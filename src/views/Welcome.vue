<template>
  <div class="welcome">
    <scroll-indicator />
    <v-container>
      <the-nav-bar />
      <v-main>
        <hero-section />
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
      ScrollToTop: () => import('@/components/sections/ScrollToTop'),
      ScrollIndicator: () => import('@/components/sections/ScrollIndicator')
    }
  }
</script>

<style scoped>
  .welcome {
    min-height: 1000vh;
  }
</style>