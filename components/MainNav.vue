<template>
  <div class="main-nav">
    
    <div class="container">
      <div class="main-nav__layout">

        <Logo/>

        <NavLevel1/>

      </div>
    </div>

  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import NavLevel1 from '~/components/NavLevel1.vue'

export default {
  name: 'MainNav',
  components: {
    Logo,
    NavLevel1
  },
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
 .main-nav 

  &__layout
    display: flex
    justify-content: space-between
    padding: 20px 0

</style>
