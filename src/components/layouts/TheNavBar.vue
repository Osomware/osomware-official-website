<template>
  <div>
    <v-app-bar flat color="white">
      <v-toolbar-title>
        <v-img src="@/assets/logo.svg" max-width="155" />
      </v-toolbar-title> <!-- BUSINESS LOGO -->
      <v-spacer></v-spacer>
      <v-btn icon
             @click="drawer = !drawer"
             v-if="isXs"
             color="darkblue">
        <v-icon class="iconify" 
                data-icon="heroicons-outline:menu-alt-4">
        </v-icon>
      </v-btn> <!-- HAMBURGER MENU -->
      <div v-else>
        <v-btn text 
               v-for="([text, link], i) in items"
               :key="i"
               color="darkblue"
               tile
               class="font-weight-bold"
               @click="$vuetify.goTo(link)">
          <span class="text-capitalize">
            {{ text }}
          </span>
        </v-btn>
      </div> <!-- NAVIGATION LINKS -->
    </v-app-bar>
    <the-side-bar :visible="drawer"
                  @close="drawer = false"
                  :navItems="items">
    </the-side-bar> <!-- SIDE NAVIGATION LINKS -->
  </div>
</template>

<script>
  export default {
    components: {
      TheSideBar: () => import('./TheSideBar')
    },
    data () {
      return {
        drawer: false,
        isXs: false,
        items: [
          ["Home", "#hero"],
          ["Services", "#services"],
          ["About", "#about"],
          ["Case Studies", "#case-studies"],
          ["Careers", "#careers"],
          ["Contact", "#contact"]
        ]
      }
    },
    methods: {
      onResize () {
        this.isXs = window.innerWidth < 940;
      }
    },
    watch: {
      isXs (value) {
        if (!value) {
          if (this.drawer) {
            this.drawer = false;
          }
        }
      }
    },
    mounted() {
      this.onResize()
      window.addEventListener("resize", this.onResize, { 
        passive: true 
      })
    }
  }
</script>

<style scoped>
  .v-toolbar {
    transition: 0.6s;
  }
</style