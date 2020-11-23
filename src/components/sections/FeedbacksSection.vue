<template>
  <section>
    <v-layout class="our-feedbacks-section">
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <div class="text-capitalize font-weight-medium blueprimary--text mb-2">Feedbacks</div>
          <div class="display-2 font-weight-black darkblue--text title-img py-4">
            Our client appreciate what we do
          </div>
        </v-col>
        <v-col cols="12">
          <v-container>
            <carousel-3d width="500" max-height="500" :autoplay="true" :autoplay-timeout="2400">
              <div v-for="(item, index) in items" :key="index">
                <slide :index="item.id">
                  <img :src="item.src"/>
                </slide>
              </div>
            </carousel-3d>
          </v-container>
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
            id: 0,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/98190909_664701934311908_289760161898168320_n.jpg?alt=media&token=cafd6f9c-c581-4785-b3d7-0887645b2bf1',
          },
          {
            id: 1,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/98195901_248009556612399_8092088538830471168_n.jpg?alt=media&token=23433c7b-9923-403c-a2b5-e2b7819b6572',
          },
          {
            id: 2,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/1.JPG?alt=media&token=ea736538-e383-4798-9306-f821531ab684',
          },
          {
            id: 3,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/97122742_231510738137230_7575093820648325120_n.jpg?alt=media&token=6b11f3ce-098d-4c7f-852e-de2335e89d45',
          },
           {
            id: 4,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/97445808_2549831308589824_8970811067743600640_n.png?alt=media&token=b51099e3-4027-4e3f-908c-b822c8c09b27',
          },
           {
            id: 5,
            src: 'https://firebasestorage.googleapis.com/v0/b/vue-twitter-abae3.appspot.com/o/portfolio-images%2Ftwitter.JPG?alt=media&token=745d86a0-f3bb-427c-a8da-ece9b3f537f0',
          },
          {
            id: 6,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/97999802_549745039045759_8802413925577523200_n.jpg?alt=media&token=9b1e16d6-ddf1-455f-bea5-b86237cdfcba',
          },
          {
            id: 7,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/100061169_554849005108547_2218268007572963328_n.jpg?alt=media&token=8d908b32-0dcf-4213-88de-bf3cd768a17b',
          },
          {
            id: 8,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/97337817_502533447300113_6904079595251695616_n.png?alt=media&token=df1e1f2a-0ac9-4d3b-aa9a-53d18fc807c5',
          },
          {
            id: 9,
            src: 'https://firebasestorage.googleapis.com/v0/b/vic-solution-admin.appspot.com/o/97414226_2521136174656232_4971303252164345856_n.jpg?alt=media&token=71297302-d2ca-433c-ab6b-0726dfb38cb0',
          }
        ]
      }
    }
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