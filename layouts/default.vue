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
  border-bottom: 1px solid #5c297e;
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
      display: flex;
      border-bottom: 2px dotted #340652;
      &:hover {
        border-color: #753c9b;
      }
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
    nav {
      position: absolute;
      left: 0;
      top: 50px;
      z-index: 5;
      display: none;
      width: 100%;
      ul {
        flex-direction: column;
        width: 100%;
        background-color: #340652;
        list-style-type: none;
        margin: 0;
        border-bottom: 1px solid #773aa0;
        li {
          display: flex;
          justify-content: center;
          &:hover {
            background-color: #5c297e;
          }
          a {
            letter-spacing: 8px;
            border: none;
            padding: 7px 0;
            display: block;
            width: 100%;
          }
        }
      }
    }
    .toggle {
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