<template>
  <div class="welcome">
    <v-container>
      <the-nav-bar />
      <v-main>
        
      </v-main>
    </v-container>
  </div>
</template>

<script>
  export default {
    name: 'welcome',
    components: {
      TheNavBar: () => import('@/components/layouts/TheNavBar')
    }
  }
</script>

<style scoped>
  .welcome {
    min-height: 1000vh;
  }
</style>