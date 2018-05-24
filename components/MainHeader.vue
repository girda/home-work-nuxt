<template>
  <div class="main-header">

    <MainNav/>

  </div>
</template>

<script>
import MainNav from '~/components/MainNav.vue'


export default {
  name: 'MainHeader',
  components: {
    MainNav,
  },
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<style lang="sass" scoped>
.main-header
  background-color: black

</style>
