<template>
  <div>
    <MainHeader/>
    <nuxt/>
    <MainFooter/>
  </div>
</template>

<script>
import MainHeader from '~/components/MainHeader.vue'
import MainFooter from '~/components/MainFooter.vue'

export default {
  components: {
    MainHeader,
    MainFooter
  }
}
</script>


<style lang="sass">

@font-face
  font-family: NexaBold
  src: url("../fonts/NexaBold.woff") format("woff")
  font-weight: normal
  font-style: normal
  font-display: swap

@font-face
  font-family: proximanova-regular
  src: url("../fonts/proximanova-regular.woff") format("woff")
  font-weight: normal
  font-style: normal
  font-display: swap

@font-face
  font-family: proximanova-semibold
  src: url("../fonts/proximanova-semibold.woff") format("woff")
  font-weight: normal
  font-style: normal
  font-display: swap

html, body 
  margin: 0
  font-family: 'proximanova-regular' , sans-serif
  font-weight: 400
  font-size: 16px
  line-height: 1.2
  color: #111111

h1,h2,h3,p,div,button
  margin: 0
  padding: 0

.container
  width: 940px
  margin: 0 auto
</style>
