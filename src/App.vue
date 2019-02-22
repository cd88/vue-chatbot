<template>
  <div id="app">
    <ChatContainer v-bind:chatLog="chatLog" />
    <ChatEntry v-on:send-chat="sendChat" id="chat-entry" />
  </div>
</template>

<script>
import ChatContainer from './components/ChatContainer.vue'
import ChatEntry from './components/ChatEntry.vue'

export default {
  name: 'app',
  components: {
    ChatContainer,
    ChatEntry
  },
  methods: {
    sendChat(newChat){
      this.chatLog.push(newChat);
    }
  },
  data() {
    return {
      chatLog: [
        { id:1,
          sender: "bot",
          direction: "received",
          message: "Chatbot isn't available right now"
        },
        { id:2,
          sender: "you",
          direction: "sent",
          message: "Chatbot isn't available right now"
        }
      ]
    }
  }
}
</script>

<style lang="sass">
#app
  width: 400px
  height: 400px
  padding: 15px
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  color: #2c3e50
  margin: 10px 5px
  display: flex
  flex-direction: column
  align-content: space-between

.chat-container



</style>
