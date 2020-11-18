<template>
  <section>
    <v-layout class="our-feedbacks-section">
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <div class="text-capitalize font-weight-black blueprimary--text mb-2">Feedbacks</div>
          <div class="display-2 font-weight-black darkblue--text title-img py-4">
            Our client appreciate what we do
          </div>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>

<style scoped lang="scss">
  .our-feedbacks-section {  
    min-height: 100vh;
    justify-content: center;
  }
  .title-img {
    background-image: url('./../../assets/svgs/circles.svg');
    background-repeat: no-repeat;
    background-position: center;
  }
</style>