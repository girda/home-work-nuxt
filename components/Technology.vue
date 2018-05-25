<template>
  <div class="technology">
    
    <div class="container">


      <NewsPost v-for="(item, i) in posts" :key="i"
        :title="item.title" 
        :date="item.date"
        :url="item.url" 
        :btn="item.btn"
        :descr1="item.descr1"
        :descr2="item.descr2">

        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
        quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
        consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
        cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
        proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>

      </NewsPost>

      <div class="technology__pagination">
        <pagination/>
      </div>

    </div>
    

  </div>
</template>

<script>
import NewsPost from '~/components/NewsPost.vue'
import Pagination from '~/components/Pagination.vue'

export default {
  name: 'Technology',
  components: {
    Pagination,
    NewsPost,
  },
  data () {
    return {
      msg: 'Technology',
      posts: [
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
  }
}
</script>


<style lang="sass" scoped>
.technology
  margin-top: 90px

  news-post:last-of-type
    background-color: black

  &__pagination
    margin-bottom: 90px
</style>
