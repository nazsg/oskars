<template>
  <div class="container2" >
    <div class="content">
      <header style="z-index: 1000">
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="about-us">About Us</nuxt-link>
        <nuxt-link to="/find-us">Find Us</nuxt-link>
        <nuxt-link to="/contact-us">Contact Us</nuxt-link>
      </header>      
      
      <!-- <p>
        blue layout
      </p> -->
      <nuxt />
    </div>
    <appFooter />
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
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

</style>