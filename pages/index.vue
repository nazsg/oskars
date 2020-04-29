<template>
  <div>
    <div id="showcase">

      <div class="banner">
        <h1 class="">Great friendly family barber shop</h1>
        <h3 class="">
  by professional staff for all styles - Hair cuts, Shape-Ups, razo shave & hot towel, beard trim. No appointment needed, just pop in.</h3>
      </div>
    </div>
    <section></section>
    <v-parallax :src="images[0]">
      <section id="opening-hours">
        <time itemprop="openingHours" datetime="Mo-We, Fr 09:00-18:00">Mondays to Wednesdays, Fridays 9am-6.00pm</time>
        <time itemprop="openingHours" datetime="Th 09:00-18:30">Thursdays 9am-6.30pm</time>
        <time itemprop="openingHours" datetime="Sa 08:30-17:30">Saturdays 8.30am-5.30pm</time>
        <time itemprop="openingHours" datetime="Su 09:30-16:00">Sundays 9.30am-4.00pm</time>
      </section>
    </v-parallax>
    <!-- <v-parallax src="~assets/img/img1.jpg"></v-parallax> -->
    <section id="">Prices</section>
    <v-parallax 
      :src="getImg('img1.jpg')"></v-parallax>
  </div>
</template>

<script>
export default {
  layout: 'blue',
  components: {
  },
  methods: {
    getImg(img) {
      return require('../assets/img/' + img)
    }
  },
  data() {
    return {
      img1: 'https://images.pexels.com/photos/1319460/pexels-photo-1319460.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260',
      images: [
        'https://images.pexels.com/photos/1319460/pexels-photo-1319460.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260',
        'https://images.pexels.com/photos/128867/coins-currency-investment-insurance-128867.jpeg?auto=compress&cs=tinysrgb&h=750&w=1260',
        'img1.jpg',
        'img2.jpg'
      ]
    }
  }
}
</script>

<style lang="scss">
$bg : rgba(72, 6, 116, 0.61);

.banner {
  background-color: $bg;
  padding: 30px 20px;
  color: rgb(236, 236, 236);
  border-radius: 15px;
  width: 100%;
}

section#opening-hours {
  background-color: $bg;
  background-image: url('https://images.pexels.com/photos/9352/glass-time-watch-business.jpg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940');
  padding: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  line-height: 1.5;
  time {
    letter-spacing: 2px;
    font-family: Roboto;
    color: white;
  }
}

#showcase {
  background-image: url('https://images.pexels.com/photos/3162022/pexels-photo-3162022.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  height: 100vh;
  padding: 0 20px;
  text-align: center;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  h1 {
    font-size: 50px;
    line-height: 1.4;
  }

  p {
    font-size: 20px;
    background-color: rgba(250, 214, 114, 0.363);
    padding: 15px;
    color: rgb(58, 58, 57);
  }

  .button {
    font-size: 18px;
    text-decoration: none;
    color: rgb(73, 75, 72);
    border: 1px solid rgb(84, 85, 80);
    background-color: rgb(206, 192, 161);
    padding: 10px 20px;
    border-radius: 10px;
    margin-top: 20px;
    &:hover {
      background-color: rgb(234, 234, 245);
    }
  }
}
</style>