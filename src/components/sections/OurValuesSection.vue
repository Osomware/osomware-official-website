<template>
  <section>
    <v-layout class="our-values-section">
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <div class="text-capitalize font-weight-medium blueprimary--text mb-2">Our Values</div>
          <div class="display-2 font-weight-black pb-6 darkblue--text title-img py-4">
            Quality is our priority
          </div>
          <div class="bluesecondary--text description">
            All our processes are customer-orientted, designed to reduce the cost of business operation, address IT 
            resourcing challenges, and offer you competitive edge. We start with a deep analysis of your requirements 
            and continue our relationship with post-launch support and updates.
          </div>
          <v-row align="center" justify="center" class="mt-10">
            <div v-for="value in core_values" :key="value.id">
              <v-hover v-slot="{ hover }" close-delay="200">
                <v-card flat :class="`${hover ? 'elevation-3' : 'elevation-1'} ma-3`">
                  <v-container class="chip-container">
                    <div class="d-flex justify-center align-center mt-3">
                      <v-img :src="getImage(value)" max-width="80"/>
                    </div>
                    <v-card-subtitle class="font-weight-medium darkblue--text">
                      {{ value.text }}
                    </v-card-subtitle>
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
        core_values: [
          { id: 1, text: 'Research and Discovery', src: require('./../../assets/svgs/core-values/icon1.svg') },
          { id: 2, text: 'Validating and Shaping Idea', src: require('./../../assets/svgs/core-values/icon2.svg') },
          { id: 3, text: 'Design and Prototyping', src: require('./../../assets/svgs/core-values/icon3.svg') },
          { id: 4, text: 'Development', src: require('./../../assets/svgs/core-values/icon3.svg') },
          { id: 5, text: 'Testing and Quality Assurance', src: require('./../../assets/svgs/core-values/icon4.svg') },
          { id: 6, text: 'Maintenance and Support', src: require('./../../assets/svgs/core-values/icon5.svg') },
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
  .our-values-section {  
    min-height: 100vh;
    justify-content: center;
  }
  .description {
    line-height: 2.5;
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
    max-width: 156px;
    min-height: 210px;
  }
</style>