<template>
  <div>
    <div class="content">
      <header>
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="about-us">About Us</nuxt-link>
        <nuxt-link to="/pictures">Pictures</nuxt-link>
        <nuxt-link to="/find-us">Find Us</nuxt-link>
      </header>
      <Nuxt />
    </div>
    <appFooter />
  </div>
</template>

<script>
import appFooter from '~/components/footer'
export default {
  components: {
    appFooter
  }
}
</script>

<style lang="scss" scoped>
* {
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
}

html, body {
  height: 100%;
}
body {
  display: flex;
  flex-direction: column;
}
.content {
  flex: 1 0 auto;
  background-color: pink;
}
#__layout > div {
  display: flex;
  flex-direction: column;
  flex: 1 0 auto;
  .content {
    flex: 1 0 auto;

  }
}
</style>
