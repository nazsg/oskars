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
        <button @click="clear">Clear</button> <button>Submit</button>
        <!-- <SendIcon :size=size /> <DeleteIcon :size=size @click="clear"/> -->
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
