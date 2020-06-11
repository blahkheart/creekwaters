<template>
  <v-app>
   <Navbar/>
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar'

export default {
  name: 'App',
  components: {Navbar},
  data: () => ({
  }),
};
</script>

<style lang="scss">
#app {
  font-family: raleway;
  button.cw-btn{
    border-radius: 3px;
    transition: all .3s ease-in-out;
    &:hover {
      background: darken(#6A4CB7, 8%) !important;
    }
    &:active {
      background: darken(#6A4CB7, 20%) !important;
    }
  }
}
</style>