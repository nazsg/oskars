<template>
  <div>
    <div id="showcase">

      <div class="banner">
        <h1>Great friendly family <br>barber shop</h1>
        <h2>
             by professional staff for all styles <br />Hair cuts, Shape-Ups, razo shave & hot towel, beard trim. <br/>No appointment needed, just pop in.</h2>
      </div>
    </div>
    <section>&nbsp;</section>
    <v-parallax src="/clock1a.jpg" height=600>
      <section id="opening-hours">
        <time itemprop="openingHours" datetime="Mo-We, Fr 09:00-18:00">Monday 9am-6.00pm</time>
        <time itemprop="openingHours" datetime="Tu 09:00-18:00">Tuesday 9am-6.00pm</time>
        <time itemprop="openingHours" datetime="We 09:00-18:00">Wednesday 9am-6.00pm</time>
        <time itemprop="openingHours" datetime="Th 09:00-18:30">Thursday 9am-6.30pm</time>
        <time itemprop="openingHours" datetime="Fr 09:00-18:00">Friday 9am-6.00pm</time>
        <time itemprop="openingHours" datetime="Sa 08:30-17:30">Saturday 8.30am-5.30pm</time>
        <time itemprop="openingHours" datetime="Su 09:30-16:00">Sunday 9.30am-4.00pm</time>
      </section>
    </v-parallax>
    <!-- <v-parallax src="~assets/img/img1.jpg"></v-parallax> -->
    <section id="">Prices</section>
    <v-parallax height=700 
      src="/scissors.jpg">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2490.7263139195184!2d1.128480115764971!3d51.37132787961298!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47d93562e44b632f%3A0x8e32eeadcda91d61!2s184%20High%20St%2C%20Herne%20Bay%20CT6%205AP!5e0!3m2!1sen!2suk!4v1589709769718!5m2!1sen!2suk" width="600" height="500" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
      </v-parallax>
  </div>
</template>

<script>
export default {
  components: {
  },
  
  data() {
    return {
    }
  }
}
</script>

<style lang="scss" >
$bg : #340652;

.banner {
  background-color: $bg;
  padding: 30px 20px;
  color: rgb(236, 236, 236);
  border-radius: 15px;
  width: 60%;
  letter-spacing: 4px;
  @media (min-width: 900px) {
    max-width: 900px;
  }
}
section {
  background: $bg;
}
section#opening-hours {
  background-color: #250129ec;
  // background-image: url('https://images.pexels.com/photos/9352/glass-time-watch-business.jpg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940');
  padding: 25px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  line-height: 1.5;
  // width: 60%;
  text-align: center;
  margin: 0 auto;
  border-radius: 10px;
  border: 1px solid rgb(106, 68, 112);
  time {
    letter-spacing: 2px;
    // font-family: Roboto;
    color: white;
    font-size: 1.4rem;
  }
  @media (max-width: 550px) {
    width: 95%;
  }
  @media (max-width: 700px) {
    width: 75%;
  }
}

#showcase {
  background-image: url('/barbers_bg_mask.jpg');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  height: 100vh;
  padding: 0 100px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  // align-items: center;

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
  @media (max-width: 550px) {
    h1 {
      font-size: 30px;
    }
    h2 {
      font-size: 18px;
    }
  }
}

iframe {
  border-radius: 10px;
  margin: 0 auto;
  width: 100%;
  opacity: 0.9;
}
</style>