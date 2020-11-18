<template>
  <section id="services">
    <v-layout class="our-services-section">
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <div class="text-capitalize font-weight-black blueprimary--text mb-2">Our Services</div>
          <div class="display-2 font-weight-black pb-6 darkblue--text title-img py-4">
            We have the skills and experience to serve you
          </div>
          <div class="darkblue--text description">
            We help client to design and develop future proof, significant and secure digital 
            products that are centered around users' need and fulfill clients' business goals.
          </div>
          <v-row align="center" justify="center" class="mt-10">
            <div v-for="value in services" :key="value.id">
              <v-hover v-slot="{ hover }" close-delay="200">
                <v-card flat :class="`${hover ? 'elevation-24' : 'elevation-0'} ma-5`">
                  <v-container class="chip-container">
                    <div class="d-flex justify-center align-center mt-3">
                      <v-img :src="getImage(value)" max-width="120"/>
                    </div>
                    <v-card-text class="font-weight-bold darkblue--text">
                      <h3>{{ value.text }}</h3>
                    </v-card-text>
                  </v-container>
                </v-card>
              </v-hover>
            </div>
          </v-row>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>

<script>
  export default {
    name: 'our-values-section',
    data () {
      return {
        services: [
          { id: 1, text: 'Software Development', src: require('./../../assets/img/services-icon/services1.png') },
          { id: 2, text: 'Multimedia Arts and Design', src: require('./../../assets/img/services-icon/services2.png') },
          { id: 3, text: 'Web Development', src: require('./../../assets/img/services-icon/services3.png') },
          { id: 4, text: 'Web Design & Development', src: require('./../../assets/img/services-icon/services4.png') },
          { id: 5, text: 'User Experience Design', src: require('./../../assets/img/services-icon/services5.png') }
        ]
      }
    },
    methods: {
      getImage (value) {
        const { src } = value
        return src
      }
    }
  }
</script>

<style scoped lang="scss">
  .our-services-section {  
    min-height: 100vh;
    justify-content: center;
  }
  .description {
    line-height: 2.5;
    opacity: 80% !important;
    @media screen and (min-width: 800px) {
      margin: 0px 100px 0px 100px;
    }
  }
  .title-img {
    background-image: url('./../../assets/svgs/circles.svg');
    background-repeat: no-repeat;
    background-position: center;
  }
  .chip-container {
    max-width: 190px;
    min-height: 240px;
  }
</style>