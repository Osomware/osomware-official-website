<template>
  <section>
    <v-layout class="our-feedbacks-section">
      <v-row align="center" justify="center">
        <v-col class="text-center">
          <div class="text-capitalize font-weight-medium blueprimary--text mb-2">Feedbacks</div>
          <div class="display-2 font-weight-black darkblue--text title-img py-4">
            Our client appreciate what we do
          </div>
          <!-- <v-card flat class="mx-auto" max-width="900">
            <v-system-bar lights-out></v-system-bar>
            <v-carousel>
              <v-carousel-item
                v-for="(item,i) in items"
                :key="i"
                :src="item.src"
                reverse-transition="fade-transition"
                transition="fade-transition"
              ></v-carousel-item>
            </v-carousel>
          </v-card> -->
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