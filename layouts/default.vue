<template>
  <div class="container2">
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
  components: { headerComp }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  // font-family: Roboto;
  // font-family: 'Chelsea Market', cursive;
  // font-family: 'Caveat Brush', cursive;
  font-family: "Fredericka the Great", cursive;
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
    // width: 50%;
    padding-left: 0;
    justify-content: space-evenly;
    a {
      color: white;
      text-decoration: none;
      letter-spacing: 3px;
      font-size: 1.3rem;
    }
  }
  .toggle {
    display: none;
  }
  @media (max-width: 715px) {
    .brand {
      display: flex;
      justify-content: space-between;
    }
    flex-direction: column;
    position: relative;
    width: 100%;
    nav {
      position: absolute;
      left: 0;
      top: 45px;
      z-index: 5;
      display: none;
      width: 100%;
      ul {
        flex-direction: column;
        width: 100%;
        background-color: #340652;
        list-style-type: none;
        margin: 0;
        li {
          margin: 0;
          padding: 5px 0;
          width: 100%;
          &:hover {
            background-color: #5c297e;
          }
          a {
            width: inherit;
            background-color: rgb(105, 102, 102);
          }
        }
      }
    }
    .toggle {
      // order: 2;
      display: block;
      color: white;
    }
  }
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
  background-image: url("/barbers_bg_light.jpg");
  background-size: cover;
  background-position: bottom left;
}
</style>