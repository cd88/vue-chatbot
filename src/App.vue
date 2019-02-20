<template>
  <div id="app">
    <ChatItem msg="Chatbot isn't available right now"/>
    <ChatEntry />
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
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
