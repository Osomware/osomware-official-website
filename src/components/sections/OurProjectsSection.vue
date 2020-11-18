<template>
  <section>
    <v-layout class="our-projects-section">
      <v-row align="center" justify="center">
        <v-col cols="12">
          <div class="text-capitalize font-weight-black blueprimary--text mb-2 text-center">Our Projects</div>
          <div class="display-2 font-weight-black pb-6 darkblue--text title-img py-4 mb-5 text-center">
            Take a look at what we've built
          </div>
          <v-row align="center" justify="center">
            <v-col cols="12" md="6" class="d-none d-md-flex">
              <v-img
                src="@/assets/svgs/projects.svg"
                class="d-block ml-auto mr-auto"
              />
            </v-col>
            <v-col cols="12" md="6">
              <div class="headline font-weight-bold darkblue--text">
                Airclass: An E-Learning App for
                None Native English Speakers
              </div>
              <v-card-actions class="my-6">
                <v-btn small 
                       tile 
                       depressed 
                       class="text-capitalize darkblue--text">
                  UX Research
                </v-btn>
                <v-btn small 
                       tile 
                       depressed 
                       class="text-capitalize darkblue--text">
                  UI Design
                </v-btn>
                <v-btn small 
                       tile 
                       depressed 
                       class="text-capitalize darkblue--text">
                  Development
                </v-btn>
              </v-card-actions>
              <div class="bluesecondary--text text-justify description">
                Airclass is an english learning web app for filipino kids who
                wants to learn english in a more efficient and friendly way. 
                Also this app is suitable for adults who needs to review 
                their english speakers who wants to learn english as well.
              </div>
              <v-hover v-slot="{ hover }">
                <v-btn color="primary"
                      class="mt-5 text-capitalize font-weight-medium rounded-lg"
                      large
                      depressed
                      :outlined="hover ? true : false">
                  Read Case Study <v-icon right>mdi-arrow-right</v-icon>
                </v-btn>
              </v-hover>
            </v-col>
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
        core_values: []
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
  .our-projects-section {  
    min-height: 100vh;
    justify-content: center;
  }
  .description {
    line-height: 2.5;
  }
  .title-img {
    background-image: url('./../../assets/svgs/circles.svg');
    background-repeat: no-repeat;
    background-position: center;
  }
  .chip-container {
    max-width: 156px;
    min-height: 200px;
  }
</style>