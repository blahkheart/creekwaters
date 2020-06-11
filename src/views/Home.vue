<template>
  <div class="home">
    <Header/>
    <v-container>
      <v-row>
        <v-col>
          <div class="text-center home-section">
            <h2>THE FASTEST WAY TO INCREASE YOUR REVENUE</h2>
            <v-container fluid>
              <v-row dense align="center">
                <v-col cols="12" md="7">
                  <p class="px-12 mr-lg-5 text-center text-sm-left mb-12 mb-md-0 text--secondary">
                    Our digital marketing agency bridges the gap for businesses that don’t have the people, resources, time or expertise to get a measurable return on digital marketing.
                  </p>
                </v-col>
                <v-col cols="12" md="5">
                  <v-card 
                    flat
                    class="mx-auto px-12 px-sm-5"
                    max-width="600"
                  >
                    <v-img
                      src="@/assets/img/social-media-01.svg"
                      class="white--text align-end"
                    >
                    </v-img>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
            <v-divider class="mt-12 mx-12"></v-divider>
          </div>
        </v-col>
      </v-row>
      <v-row
          align="center"
          justify="center"
        >
        <v-col>
          <div class="text-center home-section">
            <h2>
              ARE YOU STRUGGLING WITH MAKING DIGITAL MARKETING WORK FOR YOUR BUSINESS?
            </h2>
            <p class="headline mb-10">
              Let us do all the heavy lifting while you focus on your business.
            </p>
              <v-container fluid>
                <v-row dense align="center">
                  <v-col cols="12" md="5">
                    <v-card 
                      flat
                      class="mx-auto px-12 px-sm-5"
                      max-width="600"
                    >
                      <v-img
                        src="@/assets/img/social-media-03.svg"
                        class="white--text align-end"
                      >
                      </v-img>
                    </v-card>
                  </v-col>
                  <v-col cols="12" md="7">
                    <p class="px-12 ml-lg-5 text-center text-sm-right mt-12 mb-md-0 text--secondary">
                      Digital marketing can be overwhelming and simply slit your focus from your business and customers. We make sure you focus 100% on your products and services while we bring the customers in the door.
                    </p>
                  </v-col>
                </v-row>
            </v-container>
            <v-divider class="ma-12"></v-divider>    
            <SiteVideo class="justify-center" indetifier="7CBW0HD7Am4"/> 
          </div>
        </v-col>
      </v-row>
      <v-row
          align="center"
          justify="center"
        >
        <v-col>
          <div class="text-center home-section">
              <!-- <v-btn large rounded  class="mt-5 subtitle-2">
                Get a free social media audit for your business
              </v-btn> -->
              <button class="cw-btn subtitle-2 deep-purple white--text pa-5 text-uppercase my-5">
                Get a free social media audit for your business
              </button>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <Footer/>
  </div>
</template>

<script>
import Header from '@/components/home/Header'
import Footer from '@/components/Footer'
import SiteVideo from '@/components/home/SiteVideo'
export default {
  name: 'Home',
  components: {
    Header,
    SiteVideo,
    Footer
  },
  data: () => ({
    cards: [
      { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', flex: 6 },
      { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6 },
    ],
    isActive: false
  })
}
</script>

<style lang="scss" scoped>
  .home-section{
    h2{
      margin: 50px 0 80px;
    } 
  }
</style>