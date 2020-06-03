<template>
  <div class="home">
    <Header/>
    <v-container>
      <v-row>
        <v-col>
          <div class="text-center home-section">
            <h2>THE FASTEST WAY TO INCREASE YOUR REVENUE</h2>
            <p>
              Our digital marketing agency, based in Northern Virginia, bridges the gap for businesses that don’t have the people, resources, time or expertise to get a measurable return on digital marketing.
            </p>
            <v-divider></v-divider>
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
            <v-divider></v-divider>    
            <SiteVideo/> 
          </div>
        </v-col>
      </v-row>
        <v-row
          align="center"
          justify="center"
        >
        <v-col>
          <div class="text-center home-section">
              <v-btn large rounded class="mt-5">
                Get a free social media audit for your business
              </v-btn>
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
  }
}
</script>
