<template>
  <v-navigation-drawer v-model="show" fixed
                       src="@/assets/logo.png">
    <v-list class="justify-center">
      <v-list-item class="align-center">
        <v-img src="@/assets/logo.svg" max-width="155" />
      </v-list-item>
    </v-list> <!-- BUSINESS LOGO AND SUBTITLE -->
    <v-divider />
    <v-list>
      <v-list-item v-for="([text, link], i) in navItems"
                   :key="i"
                   link
                   @click="$vuetify.goTo(link)">
        <v-list-item-content>
          <v-list-item-title class="subtitile-1 text-center font-weight-medium white--text">{{ text }}</v-list-item-title>
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