<template>
  <div class="news">

    <nav>
      <NavLevel2/>
    </nav>

    <Technology/>

  </div>
</template>

<script>
import NavLevel2 from '~/components/NavLevel2.vue'
import Technology from '~/components/Technology.vue'

export default {
  name: 'News',
  data () {
    return {
      msg: 'News'
    }
  },
  components: {
    NavLevel2,
    Technology,
  }
}
</script>


<style lang="sass" scoped>

</style>
