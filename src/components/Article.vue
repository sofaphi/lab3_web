<template>
  <main class="text-center">
    <h1>{{news[id-1].name}}</h1>
        <v-img
          aspect-ratio="2"
          :src="require('./../assets/images/' + news[id-1].full_image)"></v-img>
    <div class='ma-15'>
        {{news[id-1].desc}}
    </div>
    <div>
      {{news[id-1].date}}
    </div>
  </main>
</template>

<script>
import news from '@/assets/articles.json'
export default {
  name: 'Article',
  props: ['id'],
  data(){
      return {
        news: news
    };
  }
}
</script>

<style scoped>

</style>