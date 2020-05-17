<template>
  <form>
    <div class="group g1">
      <label for="">Name</label> <input type="text">
    </div>
    <div class="group g1">
      <label for="">Email</label> <input type="text">
    </div>
    <div class="group g2">
      <label for="">Message</label> <textarea name="" id="" cols="30" rows="10"></textarea>
    </div>
  </form>
</template>

<script>
export default {
  layout: 'blue'
}
</script>

<style lang="scss" scoped>
form {
  width: 99%;
  border: 1px solid #000;
  margin: 20px auto;
  display: flex;
  flex-direction: column;
  font-family: Roboto;

  .group {
    display: flex;
    margin: 10px;
    border: 0px solid #000;
    // padding: 5px;

    label, input, textarea {
      padding: 10px;
      border: 1px solid rgb(168, 167, 167);
    }
    label { border: 0;}
  }
  .g1 {
    label {
      flex-basis: 20%;
    }
    justify-content: start;
  }
  .g2 {
    flex-direction: column;
  }
}
$width: 700px;
@media (min-width: $width) {
  form {
    width: $width;
  }
}
</style>