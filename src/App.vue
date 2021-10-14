<template>
  <v-app style="background: #fff">

    <Header />

  <v-main>
    <v-container fluid>
      <router-view></router-view>
    </v-container>
  </v-main>

    <Footer />
</v-app>
</template>

<script>
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default {
  name: 'App',

  components: {
    Header,
    Footer
  },

  data: () => ({
  }),
};
</script>

<style scoped>
  #app {
    max-width: 1000px;
    margin: 0 auto;
  }
</style>