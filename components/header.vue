<template>
      <header>
        <div class="brand">OSKARS BARBERS
          <a href="#" @click="expand = !expand">
            <Menu class="toggle" />
          </a>
        </div>
        <nav class="menu" :class="{expand}">
          <ul >
            <li @click="expand = false">            
              <nuxt-link to="/">Home</nuxt-link>
            </li>
            <li @click="expand = false">            
              <nuxt-link to="/pictures">Pictures</nuxt-link>
            </li>
            <li @click="expand = false">            
              <nuxt-link to="/contact-us">Contact Us</nuxt-link>
            </li>
          </ul>
        </nav>
      </header>  
</template>
<script>
import Menu from 'vue-material-design-icons/Menu.vue'
export default {
  components: { Menu },
  data() {
    return {
      expand: false
    }
  },
}
</script>
<style lang="scss" scoped>
.expand {
  display: flex;
}
</style>