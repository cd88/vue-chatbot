<template>
  <form @submit.prevent="sendMessage" class="chat-entry-form">
    <input v-model="messageDraft" placeholder="works" />
    <button type="submit" name="button">Send</button>
  </form>
</template>

<script>
import uuid from 'uuid';

export default {
  name: 'ChatEntry',
  data() {
    return {
      messageDraft: ''
    }
  },
  methods: {
    sendMessage() {
      const newChat = {
        id: uuid.v4(),
        direction: 'sent',
        sender: 'you',
        message: this.messageDraft
      }
      this.$emit('send-chat', newChat)
      this.messageDraft = ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
a
  color: #42b983

</style>
