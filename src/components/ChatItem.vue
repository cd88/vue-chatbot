<template>
  <div class="chat-item">
    <h3 v-bind:key="msg.id" v-for="msg in chatLog"
      class=msg.sender>
        {{ msg.text }}
    </h3>
  </div>
</template>

<script>
export default {
  name: 'ChatItem',
  props: {
    chatLog: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
h3
  margin: 40px 0 0

ul
  list-style-type: none
  padding: 0

li
  display: inline-block
  margin: 0 10px

a
  color: #42b983

</style>
