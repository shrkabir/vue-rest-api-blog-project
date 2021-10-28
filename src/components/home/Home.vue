<template>
    <div>
        <home-featured-blog/>
            <!-- Blog preview section-->
        <home-all-blogs-section/>
    </div>
</template>

<script>
import HomeFeaturedBlog from './HomeFeaturedBlog'
import HomeAllBlogs from './HomeAllBlogs.vue'
export default {
  name: 'VueRestApiBlogProjectHome',
  components: {
    'home-featured-blog': HomeFeaturedBlog,
    'home-all-blogs-section': HomeAllBlogs
  },

  data () {
    return {

    }
  },

  mounted () {

  },

  methods: {

  }

}
</script>

<style scoped>

</style>
