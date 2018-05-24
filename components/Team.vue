<template>
  <div class="team">
    
    <div class="container">
      <div class="team__title" @click="show = !show" style="cursor: pointer;">{{title}}</div>

      <div class="team__content">

          <PlayerItem v-for="(item, i) in players" :key="i">
            <transition name="fade">
            <Player :name="item.name" :position="item.position" :url="item.url" v-if="show">
              {{item.descr}}
            </Player>
            </transition>
          </PlayerItem>

      </div>
    </div>
    
  </div>
</template>

<script>
import PlayerItem from '~/components/PlayerItem.vue'
import Player from '~/components/Player.vue'

export default {
  name: 'Team',
  transition: 'fade',
  components: {
    PlayerItem,
    Player,
  },
  data () {
    return {
      title: 'Meet Our Team!',
      show: true,
      players: [
        {
          name: 'Kimberly Thompson',
          position: 'Founder & CEO',
          url: '/avatar.jpg',
          descr: 'Kimberly is the founder and the CEO of our company. With 10 years of experience in the tech industry, she ensures all operations are running smoothly.'
        },
        {
          name: 'Rico Masi',
          position: 'Code Master',
          url: '/avatar.jpg',
          descr: 'There’s no challege Rico can’t tame! Making sure everything is safe and secure on the back end, you can say that he’s the heart of this team.'
        },
        {
          name: 'Uku Mason',
          position: 'Marketing Expert',
          url: '/avatar.jpg',
          descr: 'Not your average marketer. Uku manages everything from, marketing and finance to customer relation.'
        },
        {
          name: 'Blaz Robar',
          position: 'Design Guru',
          url: '/avatar.jpg',
          descr: 'A Highly experienced UI/UX designer, Blaz brings our ideas to life with his beautiful visual designs.'
        },
        {
          name: 'Jamie Adams',
          position: 'Assistant',
          url: '/avatar.jpg',
          descr: 'Don’t let the picture fool you. Jamie is the glue that holds our team together! Managing everthing from recruitments, social gatherings, and everyday operations.'
        }
      ]
    }
  }
}
</script>

<style lang="sass" scoped>
.team
  margin-bottom: 30px

  &__content
    display: flex
    justify-content: center
    flex-wrap: wrap

  &__title
    font-family: NexaBold
    font-size: 48px
    text-align: center
    margin-bottom: 45px

.fade-enter-active, .fade-leave-active 
  transition: all 0.25s ease-out

.fade-enter, .fade-leave-to 
  opacity: 0
  transform: translate(0, 100px)

</style>
