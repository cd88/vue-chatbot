<template>
  <form class="chat-entry-form">
    <input placeholder="works" />
    <button type="button" name="button">Send</button>
  </form>
</template>

<script>
export default {
  name: 'ChatEntry',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
a
  color: #42b983

</style>
