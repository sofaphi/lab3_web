<template>
    <div class="text-center">
        <h1 class="without-joke">в этот раз без шутки</h1>
        <Slider/>
    </div>
</template>

<script>
import Slider from '@/components/Slider.vue'

export default {
  name: "Home",
  components: {
      Slider
  },
};
</script>

<style scoped>
span {
  color: #000;
}

h1 {
  text-transform: uppercase;
  letter-spacing: 17px;
}
</style>