<template>
  <nav class="nav-level-1">

    <nuxt-link class="nav-level-1__link" to="Blog">Blog</nuxt-link>

    <nuxt-link class="nav-level-1__link" to="News">News</nuxt-link>

<!--     <nuxt-link class="nav-level-1__link" to="Inspiration">Inspiration</nuxt-link>

    <nuxt-link class="nav-level-1__link" to="Tutorials">Tutorials</nuxt-link>

    <nuxt-link class="nav-level-1__link" to="Wordpress">Wordpress</nuxt-link> -->
      
  </nav>
</template>

<script>
export default {
  name: 'NavLevel1',
  data () {
    return {
      msg: '' 
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass">
.nav-level-1
  display: flex
  align-items: center

  &__link
    margin-left: 20px
    font-family: NexaBold
    font-size: 16px
    font-weight: 700
    color: #cccccc
    text-decoration: none
    text-transform: uppercase
    &:hover, &.router-link-active
      color: white
    

</style>
