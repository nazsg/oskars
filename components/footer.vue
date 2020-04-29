<template>
  <footer>
    <p>&copy {{ new Date().getFullYear() }}</p>
  </footer>
</template>

<style lang="scss" >

footer {
  background-color: rgb(139, 37, 37);
  height: 50px;
  // padding: 20px;
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  // color: red;
  p {
    margin: 0;
    padding: 0;
  }
}

.footer {
}
</style>