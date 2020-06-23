<template>
  <div class="contact">
    <form>
      <div class="group g1">
        <label for="">Name</label> <input type="text" v-model="name">
      </div>
      <div class="group g1">
        <label for="">Email</label> <input type="text" v-model="email">
      </div>
      <div class="group g2">
        <label for="">Message</label> <textarea name="" id="" cols="30" rows="10" v-model="message"></textarea>
      </div>
      <div class="antispam">
        <antispam v-if="result == 'unverified'" result="unverified" v-on:updateResult="result = arguments[0]" />
      </div>
      <div class="group actions">
        <SendIcon :size=size /> <DeleteIcon :size=size @click="clear"/>
      </div>
    </form>

  </div>
</template>

<script>
import SendIcon from 'vue-material-design-icons/EmailSend.vue'
import DeleteIcon from 'vue-material-design-icons/TrashCanOutline.vue'
import antispam from '~/components/antispam'
export default {
  components: { SendIcon, DeleteIcon, antispam },
  layout: 'blue',
  data() {
    return {
      name: '', email: '', message: '',
      size: 40, result: 'unverified'
    }
  },
  methods: {
    clear() {
      this.name = '', this.email = '', this.message = ''
    }
  }
}
</script>

<style lang="scss" scoped>
.contact {
  background-image: url('/email3.jpg');
  background-size: cover;
  background-position: top center;
  background-attachment: fixed;
  height: 100%;
  padding: 0 20px;
  text-align: center;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;  
}
form {
  width: 99%;
  border: 1px solid #000;
  margin: 20px auto;
  display: flex;
  flex-direction: column;
  font-family: Roboto;
  background-color: rgba(189, 132, 216, 0.884);

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
  input, textarea {
    background-color: rgba(211, 210, 210, 0.863);
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
  .actions {
    justify-content: space-evenly;
    span {
      color: rgb(75, 73, 73);
      cursor: pointer;
      &:hover {
        color: #000;
      }

    }
  }
}
$width: 700px;
@media (min-width: $width) {
  form {
    width: $width;
  }
}
</style>