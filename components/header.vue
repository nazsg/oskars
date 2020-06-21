<template>
      <header>
        <div>OSKARS BARBERS</div>
        <a href="#" @click="expand = !expand">
          <Menu class="menu" />
        </a>
        <nav :class="{expand}">
          <ul >
            <li>            
              <nuxt-link to="/">Home</nuxt-link>
            </li>
            <li>            
              <nuxt-link to="/pictures">Pictures</nuxt-link>
            </li>
            <li>            
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
  methods: {

  }
}
</script>
<style lang="scss" scoped>
.expand {
  display: flex;
  margin-top: 50px;
}
</style>