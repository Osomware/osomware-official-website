<template>
  <section>
    <v-layout class="talk-to-us-section">
      <v-row align="center" justify="center">
        <v-col cols="12" class="text-center">
          <div class="display-2 font-weight-black darkblue--text">
            Have a project in mind?
          </div>
          <v-btn depressed 
                 color="primary"
                 x-large
                 class="rounded-lg text-capitalize my-7">
            Talk to Us
          </v-btn>
        </v-col>
      </v-row>
    </v-layout>
  </section>
</template>

<style scoped lang="scss">
  .talk-to-us-section {  
    min-height: 50vh;
    justify-content: center;
  }
</style>