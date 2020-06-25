<template>
  <footer>
    <ul>
      <li>
        &copy {{ new Date().getFullYear() }} Oskars Barbers
      </li>
      <li>
        184 high street Herne Bay, Kent CT6 5AP       
      </li>
  
      <li>
        <phoneIcon />
        <a href="tel:07447 008787">07447 008787</a> 
      </li> 
      <li>
        Follow us: <a href="http://www.facebook.com/oskarsbarbers" target="oskars">
         <Facebook />
        </a>
      </li>
    </ul>
  </footer>
</template>
<script>
import phoneIcon from 'vue-material-design-icons/Phone.vue'
import Facebook from 'vue-material-design-icons/Facebook.vue'
export default {
  components: { phoneIcon, Facebook }
}
</script>
<style lang="scss" scoped>

footer {
  li:first-child, li:nth-child(2) {
  text-transform: uppercase;
  }
  font-size: 1.3rem;
  width: 100%;
  border-top: 2px solid #5f327e;
  background-color: #340652;
  padding: 20px 0;
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: space-around;
  color: rgb(180, 177, 177);
  ul {
    width: 90%;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-between;
    list-style-type: none;
    @media (max-width: 750px) {
      flex-direction: column;
      justify-content: center;
      align-items: center;
      li {
        padding: 5px 0;
      }
    }
    a {
      color: #999;
      text-decoration: none;
      &:hover {
        color: rgb(184, 11, 236);
      }
    }
  }
}

</style>