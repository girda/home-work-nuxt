<template>
  <section class="news-post" :data-mod="mod">
    
    <div class="container">
      
      <div class="news-post__title">{{title}}</div>

      <div class="news-post__date">Posted on {{date}}</div>

      <div class="news-post__img">
        <img :src="url">
      </div>

      <div class="news-post__descr">
        <slot></slot>
        <transition name="fade">
          <div v-if="show">
            <p>{{descr1}}</p>
            <p>{{descr2}}</p>
          </div>
        </transition>
      </div>

      <button v-if="btn" class="news-post__btn" @click="show = !show">
        <span class="news-post__btn-icon">
          <img src="/arrow2.svg">
        </span>
        <span v-if="!show">Read More</span>
        <span v-else>Hide</span>
      </button>

    </div>
    

  </section>
</template>

<script>
export default {
  name: 'NewsPost',
  transition: 'fade',
  props: ['title', 'date', 'url','btn', 'mod', 'descr1', 'descr2'],
  data () {
    return {
      msg: 'NewsPost',
      show: false
    }
  },
  components: {

  }
}
</script>


<style lang="sass" scoped>
.news-post
  margin-bottom: 45px
  padding-bottom: 40px
  border-bottom: 1px solid #d4d4d4
  transition: height 1s ease
  &[data-mod*=border-none]
    border: none

  &__title
    max-width: 840px
    margin: 0 auto 30px
    
    font-family: NexaBold
    font-size: 50px
    text-transform: capitalize
    text-align: center

  &__date
    margin-bottom: 50px
    font-size: 12px
    color: #8f8f8f
    text-align: center

  &__img
    display: flex
    justify-content: center
    align-items: center
    margin-bottom: 45px

    img
      width: auto
      height: auto
      max-width: 100%
      max-height: 400px
      object-fit: cover

  &__descr
    line-height: 1.6
    p
      margin-bottom: 25px
      

  &__btn
    display: flex
    align-items: center
    text-decoration: none
    color: black
    background-color: transparent
    border: none
    cursor: pointer
    outline: none

    margin-top: 40px

  &__btn-icon
    display: flex
    justify-content: center
    align-items: center
    width: 28px
    height: 28px
    margin-right: 14px

    border: 2px solid black
    border-radius: 50%
    img
      width: 20px
      height: 20px
      transform: rotate(180deg)

.fade-enter-active
  transition: all 0.5s ease-out
  // animation-name: example
  // animation-duration: 1s

.fade-leave-active 
  transition: all 0.5s ease-out
  // animation-name: example2
  // animation-duration: 2s

.fade-enter
  opacity: 0
  transform: translate(0, -100px)
  
.fade-leave-to
  opacity: 0
  transform: translate(0, 100px)

// @keyframes example 
//     from 
//       height: 0
//     to 
//       height: 150px

// @keyframes example2 
//     from 
//       height: 150px
//     to 
//       height: 0

</style>
