<template>
  <div class="player-item">
    <slot/>
  </div>
</template>

<script>
export default {
  name: 'PlayerItem',
  components: {
  },
  data () {
    return {
      msg: 'Hello from Players'
    }
  }
}
</script>

<style lang="sass" scoped>
.player-item
  margin: 0 40px 65px  

</style>
