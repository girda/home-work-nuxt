<template>
  <div class="technology">

    <div class="container">

      <div class="search">
        <input type="text" class="search__input" v-model="search" placeholder="search posts...">
      </div>

      <transition-group name="scale">
        <NewsPost v-for="(post, i) in filteredList" :key="i"
          :title="post.title" 
          :date="post.date"
          :url="post.url" 
          :btn="post.btn"
          :descr1="post.descr1"
          :descr2="post.descr2">

          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
          tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
          quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
          consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
          cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
          proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

        </NewsPost>
      </transition-group>

      <div class="technology__pagination">
        <pagination/>
      </div>

    </div>
    

  </div>
</template>

<script>
import NewsPost from '~/components/NewsPost.vue'
import Pagination from '~/components/Pagination.vue'
// import Search from '~/components/Search.vue'

export default {
  name: 'Technology',
  transition: 'scale',
  components: {
    Pagination,
    NewsPost,
    // Search,
  },
  data () {
    return {
      search: '',
      msg: 'Technology',
      postList: [
        {
          title: 'Our favourite task management app!',
          date: 'March 28, 2013',
          url: '/grunt.png',
          btn: 'true',
          descr1: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          descr2: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          title: 'Our favourite task management app!',
          date: 'March 28, 2013',
          url: '/macbook.png',
          btn: 'true',
          descr1: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          descr2: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          title: 'Our favourite task management app!',
          date: 'March 28, 2013',
          url: '/comp.png',
          btn: 'true',
          descr1: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          descr2: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          title: 'Our favourite task management app!',
          date: 'March 28, 2013',
          url: '/grunt.png',
          btn: 'true',
          descr1: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          descr2: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          title: 'Our favourite task management app!',
          date: 'March 28, 2013',
          url: '/macbook.png',
          btn: 'true',
          descr1: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          descr2: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        },
        {
          title: 'Our favourite task management app!',
          date: 'March 28, 2013',
          url: '/comp.png',
          btn: 'true',
          descr1: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          descr2: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
        }
      ]
    }
  },
  computed: {
    filteredList() {
      return this.postList.filter( post => {
        return post.title.toLowerCase().includes(this.search.toLowerCase())
      })
    }
  }
}
</script>


<style lang="sass" scoped>
.technology
  position: relative
  margin-top: 90px

  &__pagination
    margin-bottom: 90px

.search
  position: absolute
  top: -50px
  left: 50%
  transform: translateX(-50%)

  border: 1px solid #d4d4d4

  input 
    padding: 10px
    border: none
    outline: none

.scale-enter-active
  transition: all 0.5s ease-out
  animation-name: scale
  animation-duration: 0.6s

.scale-leave-active 
  transition: all 0.5s ease-out
  animation-name: scale2
  animation-duration: 0.6s


@keyframes scale 
    0%   
      opacity: 0
      transform: scale(0)

    50%  
      transform: scale(1.1)

    100% 
      opacity: 1
      transform: scale(1)
      
@keyframes scale2 
    0%   
      opacity: 1
      transform: scale(1)

    100% 
      opacity: 0
      transform: scale(0)
</style>
