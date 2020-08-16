<template>
  <div>
    <div id="showcase">

      <div class="banner">
        <h1>Great friendly family <br>barber shop</h1>
        <h2>
             by professional staff <br> for all styles <br /><br/>Hair cuts, Shape-Ups, razo shave & hot towel, beard trim. No appointment needed, just pop in.</h2>
      </div>
    </div>
    <section>&nbsp;</section>
    <v-parallax src="https://oskarsbarbers4men.co.uk/img/clock1a.jpg" height=600>
      <section id="opening-hours" itemscope itemtype="http://schema.org/openingHours">
        <template v-for="(h,index) in hours">
          <time itemprop="openingHours" :datetime="h.day_code + ' ' + 
            h.start.slice(0,2) + ':' + h.start.slice(2) + '-' + 
            h.end.slice(0,2) + ':' + h.end.slice(2)" 
            :key="index">
            {{h.day}} {{h.start | convertHours}} to  {{h.end | convertHours }}
          </time>
        </template>
      </section>
    </v-parallax>
    <!-- <v-parallax src="~assets/img/img1.jpg"></v-parallax> -->
    <section>&nbsp;</section>
    <v-parallax src="https://oskarsbarbers4men.co.uk/img/cost.jpg" height=500>
      <section id="cost">
        <ul>
          <li v-for="(p,index) in prices" :key="index">
            {{p.item}} <span>&pound; {{p.price}}</span>
          </li>
        </ul>

      </section>
    </v-parallax>
    <section>&nbsp;</section>
    <v-parallax height=700 
      src="https://oskarsbarbers4men.co.uk/img/scissors.jpg">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2490.7263139195184!2d1.128480115764971!3d51.37132787961298!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47d93562e44b632f%3A0x8e32eeadcda91d61!2s184%20High%20St%2C%20Herne%20Bay%20CT6%205AP!5e0!3m2!1sen!2suk!4v1589709769718!5m2!1sen!2suk" width="600" height="500" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
    </v-parallax>
  </div>
</template>

<script>
// import moment from 'moment'
export default {  
  head: {
    title: 'Oskars Barbers, in Herne Bay Kent',
    meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { hid: 'description', name: 'description', content: 'Barbers for men in the high street of Herne Bay in Kent.' }
    ]
  },  
  data() {
    return {
      hours: '',
      prices: '',
      test1: 'hello'
    }
  },
  filters: {
    convertHours(f) {
      var timeString = f.slice(0,2) + ':' + f.slice(2)
      var H = +timeString.substr(0, 2);
      var h = H % 12 || 12;
      var ampm = (H < 12 || H === 24) ? "am" : "pm";
      timeString = h + timeString.substr(2, 3) + ampm;
      return timeString
    }
  },
  methods: {
    getHours() {
      this.$axios.get('https://oskarsbarbers4men.co.uk/indexAPI_hours.php')
      .then(res => {
        this.hours = res.data
      })
    },
    getPrices() {
      this.$axios.get('https://oskarsbarbers4men.co.uk/indexAPI.php')
      .then(res => {
        this.prices = res.data
      })
    },
  },
  mounted() {
    this.getHours()
    this.getPrices()
    // console.log(moment('20200810').format('dddd'))
    // console.log(moment()) // now
    // console.log(moment().format('hh:mm LT'))
    // console.log('convert', moment('1830', 'hh').format('hh:mm:ss LT'))
  }
}
</script>
