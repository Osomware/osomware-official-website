<template>
  <section id="hero">
    <v-layout class="hero-container">
      <v-row align="center" justify="center">
        <v-col cols="12">
          <v-row align="center" justify="center">
            <v-col cols="12" md="6">
              <div class="bg-image"></div>
              <h1 class="display-3 font-weight-black pb-6 darkblue--text">Software development that fits your needs</h1>
              <p class="bluesecondary--text description">
                Full scale project development - Concept, 
                Architecture, Planning, UX/UI Design, Development, 
                QA and Project Management
              </p>
              <v-card-actions>
                <v-btn color="primary"
                      class="mt-5 text-capitalize font-weight-medium rounded-lg"
                      x-large
                      dark
                      width="160"
                      depressed>
                  Get a quote
                </v-btn>
                <v-hover v-slot="{ hover }">
                  <v-btn :outlined="!hover"
                          depressed
                          dark
                          color="rgb(105, 36, 255)"
                          class="mt-5 text-capitalize font-weight-medium rounded-lg"
                          x-large
                          width="160">
                    Portfolio
                  </v-btn>
                </v-hover>
              </v-card-actions>
            </v-col>
            <v-col cols="12" md="6" class="d-none d-md-flex mt-10">
              <v-img
                src="@/assets/svgs/hero.svg"
                class="d-block ml-auto mr-auto"
                max-width="800"
              />
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>

<style scoped>
  .hero-container {
    min-height: 91vh !important;
  }
  .description {
    line-height: 2.0;
  }
</style>