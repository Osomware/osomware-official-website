<template>
  <v-scale-transition>
    <v-hover v-slot="{ hover }">
      <v-btn fab
            v-show="fab"
            v-scroll="onScroll"
            dark
            fixed
            bottom
            right
            :outlined="!hover"
            color="primary elevation-24"
            @click="toTop">
          <v-icon class="iconify" data-icon="dashicons:arrow-up-alt2"></v-icon>
      </v-btn>
    </v-hover>
  </v-scale-transition>
</template>

<script>
  export default {
    name: 'scroll-to-top',
    data () {
      return {
        fab: null
      }
    },
    created() {
      const top = window.pageYOffset || 0
      if (top <= 60) {
        this.color = "transparent"
        this.flat = true
      }
    },
    watch: {
      fab(value) {
        if (value) {
          this.color = "secondary"
          this.flat = false
        } else {
          this.color = "transparent"
          this.flat = true
        }
      }
    },
    methods: {
      onScroll(e) {
      if (typeof window === "undefined") return;
        const top = window.pageYOffset || e.target.scrollTop || 0
        this.fab = top > 60
      },
      toTop() {
        this.$vuetify.goTo(0)
      }
    }
  }
</script>