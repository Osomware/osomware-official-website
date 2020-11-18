<template>
  <section id="about">
    <v-layout class="about-us-section">
      <v-row align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="6" class="d-none d-md-flex">
              <v-img
                src="@/assets/svgs/about-us.svg"
                class="d-block ml-auto mr-auto"
                max-width="800"
              />
            </v-col>
            <v-col cols="12" md="6">
              <div class="text-capitalize font-weight-black blueprimary--text mb-2">About Us</div>
              <div class="display-2 font-weight-black pb-6 darkblue--text title-img">
                What makes us <br />different?
              </div>
              <div class="bluesecondary--text text-justify description">
                Osomware offers our customer a wealth of technical <br />
                and business expertise. We create diverse, complex, <br />
                web and mobile solutions for any business need.
                <br>
                <br>
                Our knowledge and expertise translate to added <br>
                value and peace of mind for our customers. width <br>
                Syberry you get quality software and perfect service <br>
                everytime.
              </div>
              <v-hover v-slot="{ hover }">
                <v-btn color="primary"
                       class="mt-5 text-capitalize font-weight-medium rounded-lg"
                       large
                       depressed
                       :outlined="hover ? true : false">
                  Learn More <v-icon right>mdi-arrow-right</v-icon>
                </v-btn>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>

<style scoped>
  .about-us-section {  
    min-height: 100vh;
  }
  .description {
    line-height: 2.0;
  }
  .title-img {
    background-image: url('./../../assets/svgs/circles.svg');
    background-repeat: no-repeat;
  }
</style>