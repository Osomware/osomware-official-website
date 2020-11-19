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
             color="darkblue"
             large>
        <v-icon class="iconify" data-icon="heroicons-outline:menu-alt-4"></v-icon>
      </v-btn> <!-- HAMBURGER MENU -->
      <div v-else>
        <v-hover v-slot="{ hover }"
                 v-for="([text, link], i) in items"
                :key="i">
          <v-btn text 
                 tile
                 color="darkblue"
                 active-class="no-active"
                 @click="$vuetify.goTo(link)">
            <span :class="`${hover ? 'nav-link' : ''} ${text === 'Home' ? 'current' : ''} text-capitalize`">
              {{ text }}
            </span>
          </v-btn>
        </v-hover>
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
        hovered: false,
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
  .nav-link {
    position: relative;
  }
  .nav-link::before, .current::before {
    content: '';
    position: absolute;
    left: 0;
    bottom: -.5rem;
    background-color: #6924ff;
    width: 100%;
    height: 1px;
    -webkit-transform: scaleX(0);
            transform: scaleX(0);
    -webkit-transform-origin: left;
            transform-origin: left;
    -webkit-transition: -webkit-transform 650ms;
    transition: -webkit-transform 650ms;
    transition: transform 650ms;
    transition: transform 650ms, -webkit-transform 650ms;
  }
  .current::before {
    -webkit-transform: scaleX(1);
            transform: scaleX(1);
  }
  .nav-link:hover::before {
    -webkit-transform: scaleX(1);
            transform: scaleX(1);
  }
  .v-btn::before {
    background-color: transparent;
  }
  .v-btn:hover:before, .v-btn:focus:before, .v-btn:hover, .v-btn:focus  {
    background: none;
  }
</style>