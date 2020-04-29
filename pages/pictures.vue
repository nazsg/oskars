<template>
  <div id="app">
    <CoolLightBox 
      :items="items" 
      :index="index"
      @close="index = null">
    </CoolLightBox>

    <div class="images-wrapper">
      <div
        class="image"
        v-for="(image, imageIndex) in items"
        :key="imageIndex"
        @click="index = imageIndex"
        :style="{ backgroundImage: 'url(' + image + ')' }"
      ></div>
    </div>
  </div>
</template>

<script>
import CoolLightBox from 'vue-cool-lightbox'
import 'vue-cool-lightbox/dist/vue-cool-lightbox.min.css'

export default {
  data() {
    return {
      items: [
        'https://oskarsbarbers4men.co.uk/img/pic8.jpg',
        'https://oskarsbarbers4men.co.uk/img/pic10.jpg'
      ],
      index: null
    }
  },

  components: {
    CoolLightBox
  }
}
</script>

