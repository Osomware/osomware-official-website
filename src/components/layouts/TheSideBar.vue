<template>
  <v-navigation-drawer v-model="show" 
                       app
                       temporary
                       dark
                       src="@/assets/img/bgDrawer2.jpg">
    <v-list nav>
      <v-list-item class="d-flex justify-center">
        <v-img src="@/assets/logo2.svg" max-width="155" />
      </v-list-item>
    </v-list> 
    <v-divider></v-divider>
    <v-list nav class="mt-2">
      <v-list-item v-for="([text, link], i) in navItems"
                   :key="i"
                   @click="$vuetify.goTo(link)">
        <v-list-item-content>
          <v-list-item-title class="text-center">{{ text }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
  export default {
    name: 'the-side-bar',
    props: {
      visible: {
        type: Boolean,
        required: true
      },
      navItems: {
        type: Array,
        required: true
      }
    },
    computed: {
      show: {
        get () {
          return this.visible
        },
        set (value) {
          if (!value) {
            this.$emit('close')
          }
        }
      }
    }
  }
</script>