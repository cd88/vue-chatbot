<template>
  <div id="app">
    <ChatItem v-bind:chatLog="chatLog"/>
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
        { user: "bot", text: "Chatbot isn't available right now" }
      ]
    }
  }
}
</script>

<style>
#app {
  height: 400px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-content: space-between;
}
#chat-entry {
}
</style>
