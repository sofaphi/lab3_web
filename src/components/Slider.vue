<template>
  <v-carousel
    cycle
    height="400"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(article, i) in slides"
      :key="i"
    > 
      <router-link :to="'/article/' + article.id">
        <v-sheet
          :color="colors[i]"
          height="100%"
          v-if="article.slider"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="text-h4">
              {{ article.name }}
            </div>
          </v-row>
        </v-sheet>
      </router-link>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
  import news from '../assets/articles.json';
  const slides = news.filter(item => item.slider === true);

  const colors = [
    'purple lighten-4',
    'blue accent-1',
    'teal lighten-4',
    'lime lighten-4',
    'orange lighten-4',
    'blue-grey lighten-4'
];
  
  export default {
    data () {
      return {
        slides,
        colors,
      }
    },
  }
</script>

<style>
.v-application a {
  text-decoration: none;
  
}
</style>