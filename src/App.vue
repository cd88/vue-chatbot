<template>
  <div id="app">
    <div class="chat-container">
      <ChatItem v-bind:chatLog="chatLog"/>
    </div>
    <ChatEntry id="chat-entry" />
  </div>
</template>

<script>
import ChatItem from './components/ChatItem.vue'
import ChatEntry from './components/ChatEntry.vue'

export default {
  name: 'app',
  components: {
    ChatItem,
    ChatEntry
  },
  data() {
    return {
      chatLog: [
        { id:1, sender: "bot", text: "Chatbot isn't available right now" },
        { id:2, sender: "you", text: "Chatbot isn't available right now" }
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
  text-align: center
  color: #2c3e50
  margin-top: 60px
  display: flex
  flex-direction: column
  align-content: space-between

.chat-container



</style>
