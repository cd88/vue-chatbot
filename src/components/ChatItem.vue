<template>
  <div v-bind:class="chatItem.direction"
    class="chat-item">
      <span>
          {{ chatItem.message }}
      </span>
  </div>
</template>

<script>
export default {
  name: 'ChatItem',
  props: {
    chatItem: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.chat-item
  color: white
  display: flex
  width: auto
  max-width: 240px

  span
    padding: 5px 9px
    border-radius: 9px

  &.sent
    justify-content: flex-end
    margin: 0 16px 0 auto

    span
      background-color: #22CC66

  &.received
    justify-content: flex-start
    margin: 0 auto 0 16px

    span
      background-color: #CC3388
</style>
