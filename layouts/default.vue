<template>
  <div class="container2" >
    <div class="content">
      <headerComp />
      <nuxt />
    </div>
    <appFooter />
  </div>
</template>

<script>
import headerComp from "~/components/header";
export default {
  components: { headerComp },

};
</script>

<style lang="scss">

@font-face {
  font-family: 'Algerian';
  src: url('/alger.ttf');
}

* {
  margin: 0;
  // padding: 0;
  font-family: Roboto;
  // font-family: 'Chelsea Market', cursive;
  // font-family: 'Caveat Brush', cursive;
  // font-family: "Fredericka the Great", cursive;
}
html {
  overflow: auto;
}
.container2 {
  display: flex;
  flex-direction: column;
  height: 100vh;
}
.content {
  flex: 1 0 auto;
}
footer {
  color: green;
}


.pictures {
  section {
    padding: 20px;
    padding-top: 60px;
    background: none;
    @media (min-width: 800px) {
      width: 600px;
      margin: 0 auto;
    }
  }
  height: 100%;
  background-image: url("https://oskarsbarbers4men.co.uk/img/barbers_bg_light.jpg");
  background-size: cover;
  background-position: bottom left;
}

@import '~/assets/styles/home';
@import '~/assets/styles/header';
@import '~/assets/styles/contact-us';
</style>