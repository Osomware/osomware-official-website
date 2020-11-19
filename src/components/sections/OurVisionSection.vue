<template>
  <section>
    <v-layout class="our-vision-section">
      <v-row align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="6">
              <div class="text-capitalize font-weight-medium blueprimary--text mb-2">Our Vision</div>
              <div class="display-2 font-weight-black pb-6 darkblue--text title-img py-4">
               Meet Our Awesome Team
              </div>
              <div class="bluesecondary--text text-justify description">
                Need an entire development team, maybe and additional 
                development unit or just small supplemental development team
                for special projects that are outside of your core business?  if so,
                consider a dedicated team from Osomware
                <br>
                <br>
                You can ramp up in a hurry by leveraging the methodologies
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
            <v-col cols="12" md="6" class="d-none d-md-flex">
              <v-img
                src="@/assets/img/team.png"
                class="d-block ml-auto mr-auto"
                max-width="600"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>

<style scoped>
  .our-vision-section {  
    min-height: 100vh;
  }
  .description {
    line-height: 2.5;
  }
  .title-img {
    background-image: url('./../../assets/svgs/circles.svg');
    background-repeat: no-repeat;
  }
</style>