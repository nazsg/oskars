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
