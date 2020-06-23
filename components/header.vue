<template>
  <header>
    <div class="brand">
      OSKARS BARBERS
      <a href="#" @click="expand = !expand">
        <Menu class="toggle" />
      </a>
    </div>
    <nav class="menu" :class="{expand}">
      <ul>
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
import Menu from "vue-material-design-icons/Menu.vue";
export default {
  components: { Menu },
  data() {
    return {
      expand: false
    };
  },
  methods: {
    onResize(event) {
      // console.log("window has been resized", event);
      this.expand = false
    }
  },

  mounted() {
    // Register an event listener when the Vue component is ready
    window.addEventListener("resize", this.onResize);
  },

  beforeDestroy() {
    // Unregister the event listener before destroying this Vue instance
    window.removeEventListener("resize", this.onResize);
  }
};
</script>
<style lang="scss" scoped>
.expand {
  display: flex;
}
</style>