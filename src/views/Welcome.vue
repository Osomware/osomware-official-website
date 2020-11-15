<template>
  <div class="welcome">
    <the-nav-bar />
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