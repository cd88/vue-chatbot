<template>
  <div class="chat-container">
    <ChatItem v-for="chatItem in chatLog"
      v-bind:chatItem="chatItem" />
  </div>
</template>

<script>

import ChatItem from './ChatItem.vue'

export default {
  name: 'ChatContainer',
  components: {
    ChatItem
  },
  props: {
    chatLog: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.chat-container
  min-height: 160px
  max-height: 260px
  overflow-y: scroll
</style>
