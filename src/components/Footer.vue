<template>
    <v-footer
      dark
      padless
    >
      <v-card
        flat
        tile
        class="indigo darken-4 white--text text-center"
      >
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon[0]"
            class="mx-4 white--text"
            icon
            route   
            :to="icon[1]"
            target="_blank"
          >
            <v-icon size="24px">{{ icon[0] }}</v-icon>
          </v-btn>
        </v-card-text>
  
        <v-card-text class="white--text pt-0">
            We’re a digital marketing and advisory firm located in Port Harcourt, Nigeria 
            and serving clients nationally and internationally. Driven by the success of our clients, 
            we take great pride in the online strategies we help you implement to drive 
            website traffic.
        </v-card-text>
  
        <v-divider></v-divider>
  
        <v-card-text class="white--text">
         <v-icon>copyright</v-icon> <strong>{{ new Date().getFullYear() }} CreekWaters</strong>
        </v-card-text>
      </v-card>
    </v-footer>
</template>

<script>
export default {
    data: ()=> ({
        icons: [
            ['mdi-facebook', 'https://facebook.com/creekwatersdigital'],
            ['mdi-twitter', 'twitter.com'],
            ['mdi-instagram', 'https://instagram.com']
        ]
    })
}
</script>