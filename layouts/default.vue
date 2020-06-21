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
import headerComp from '~/components/header'
export default {
  components: { headerComp }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  // font-family: Roboto;
  // font-family: 'Chelsea Market', cursive;
  // font-family: 'Caveat Brush', cursive;
  font-family: 'Fredericka the Great', cursive;
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

header {

  display: flex;
  justify-content: space-between;
  background-color: #340652;
  padding: 10px 20px;
  div {
    color: white;
    font-family: Algerian;
    letter-spacing: 5px;
    font-size: 1.5rem;
  }
  ul {
    // background-color: #fff;
    display: flex;
    width: 50%;
    justify-content: space-evenly;
    a {
      color: white;
      text-decoration: none;
      letter-spacing: 3px;
      font-size: 1.3rem;
    }
  }
  .menu {
    display: none;
  }
  @media (max-width: 715px) {
    flex-direction: column;
    position: relative;
    nav {
      position: absolute;
      z-index: 2;
      display: none;    
      width: 100%;
      ul {
        flex-direction: column;
        width: 100%;
        background-color: rgb(148, 138, 138);
        li {
        width: 100%;
          a {
            width: 100%;
          }
        }
      }
    }
    .menu {
      // order: 2;
      display: block;
      color: white;
    }
    div {
      // order: 1;
    }
  }  
}

.pictures {
  section {
    padding-top: 60px;
    background: none;
    width: 600px;
    margin: 0 auto;
  }
  height: 100%;
  background-image: url('/barbers_bg2.jpg');
  background-size: cover;
  background-position: bottom left;
}

</style>