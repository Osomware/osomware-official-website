<template>
  <v-card color="#181818" flat tile>
    <v-footer flat 
              dark 
              color="#181818"
              class="container py-12">
      <v-img src="@/assets/logo2.svg" max-width="210" />
      <v-spacer></v-spacer>
      <p class="mt-5 mr-3 d-none d-md-flex title font-weight-light">Get a free consultation</p>
      <v-btn class="rounded-lg"
              color="primary" 
              depressed
              large>
        Contact
      </v-btn>
    </v-footer>
    <v-divider></v-divider>
    <v-footer flat 
              dark 
              color="#181818"
              class="container py-12">
      <v-row align="center" justify="center">
        <v-col cols="12" lg="3" md="3" sm="12">
          <p class="title font-weight-light">Subscribe to our newsletter</p>
          <v-text-field label="Email Address"
                        class="font-weight-light">
          </v-text-field>
        </v-col>
        <v-col cols="12" lg="9" md="9" sm="12">
          <v-row>
            <v-col>
              <ul>
                <li v-for="(service, index) in services" :key="index">
                  <span v-if="service.text === 'Services'" class="subtitle">{{ service.text }}</span>
                  <span v-else class="font-weight-light subtitle-2">
                    <router-link :to="service.to" class="link-to">{{ service.text }}</router-link>
                  </span>
                </li>
              </ul>
            </v-col>
            <v-col>
              <ul>
                <li v-for="(ab, index) in about" :key="index">
                  <span v-if="ab.text === 'About'" class="subtitle">{{ ab.text }}</span>
                  <span v-else class="font-weight-light subtitle-2">
                    <router-link :to="ab.to" class="link-to">{{ ab.text }}</router-link>
                  </span>
                </li>
              </ul>
            </v-col>
            <v-col>
              <ul>
                <li v-for="(he, index) in help" :key="index">
                  <span v-if="he.text === 'Help'" class="subtitle">{{ he.text }}</span>
                  <span v-else class="font-weight-light subtitle-2">
                    <router-link :to="he.to" class="link-to">{{ he.text }}</router-link>
                  </span>
                </li>
              </ul>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-footer>
    <v-footer flat 
              dark 
              color="#181818"
              class="container pb-12">
      <v-row>
        <v-col cols="12" sm="6">
          <div class="company-link">
            <a href="#" class="mx-5 subtitle-2 font-weight-light">Terms & Condition</a>
            <a href="#" class="subtitle-2 font-weight-light">Privacy Policy</a>
          </div>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon>
              <v-icon>mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
            <v-btn icon>
              <v-icon>mdi-instagram</v-icon>
            </v-btn>
          </v-card-actions>
        </v-col>
      </v-row>
    </v-footer>
  </v-card>
</template>

<script>
  export default {
    name: 'the-foot-bar',
    data () {
      return {
        services: [
          { text: 'Services' },
          { text: 'Web Development', to: '/web-development' },
          { text: 'UX/UI Design', to: '/ui-ux-design' },
          { text: 'Multimedia', to: '/multimedia' }
        ],
        about: [
          { text: 'About' },
          { text: 'Our Story', to: '/our-story' },
          { text: 'Location', to: '/location' },
          { text: 'Team', to: '/team' },
          { text: 'Career', to: '/career' }
        ],
        help: [
          { text: 'Help' },
          { text: 'FAQs', to: '/faqs' },
          { text: 'Contact US', to: '/contact-us' }
        ]
      }
    }
  }
</script>

<style scoped lang="scss">
  .theme--light.v-divider {
    border-color: rgb(236 236 236 / 12%) !important;
  }
  ul {
    list-style: none;
    li {
      margin: 20px 0;
      .link-to {
        text-decoration: none;
        color: #dcdcdc;
      }
      .link-to:hover {
        text-decoration: underline; 
        color: #fff;
      }
    }
  }
  .company-link {
    a {
      text-decoration: none;
      color: #dcdcdc;
    }
    a:hover {
      text-decoration: underline; 
      color: #fff;
    }
  }
</style>