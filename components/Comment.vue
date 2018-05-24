<template>
  <div class="comment" :data-mod="mod">
    
    <div class="comment__icon">
      <img :src="url">
    </div>

    <div class="comment__wrapper">
      
      <div class="comment__name">{{name}}</div>

      <div class="comment__date">{{date}}</div>

      <div class="comment__descr"><slot></slot></div>

      <a href="#" class="comment__btn">
        <span class="comment__btn-icon">
          <svg fill="#555555" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 90 68" xml:space="preserve">
            <path d="M90,68c0,0-10-48.7-53.9-48.7V0L0,32.3l36.1,33.5V43.9C59.9,43.9,77.6,46.1,90,68z"/>
          </svg>
        </span>
        <span class="comment__btn-text">Click to Reply</span>
      </a>

    </div>

  </div>
</template>

<script>
export default {
  name: 'Comment',
  props: ['url', 'name', 'date', 'mod'],
  data () {
    return {
    }
  }
}
</script>


<style lang="sass" scoped>
.comment
  position: relative
  padding-top: 15px
  &[data-mod*=reply]
    margin-left: 95px

  &__icon
    position: absolute
    top: 0
    left: 0px
    width: 70px
    height: 70px

    background-color: #000000
    border-radius: 50%
    overflow: hidden
    img
      max-width: 100%
      height: 100%
      object-fit: cover

  &__wrapper
    display: flex
    flex-direction: column
    padding-left: 95px

  &__name
    margin-bottom: 12px
    font-family: proximanova-semibold
    font-size: 24px

  &__date
    margin-bottom: 15px

    font-size: 14px
    color: #555555

  &__descr
    line-height: 1.4
    margin-bottom: 5px

  &__btn
    display: flex
    font-size: 16px
    color: #555555
    text-decoration: none

  &__btn-icon
    display: flex
    margin-right: 5px
    svg
      width: 20px
      height: 16px
    

</style>
