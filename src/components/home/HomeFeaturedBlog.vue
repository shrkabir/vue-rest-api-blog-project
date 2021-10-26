<template>
    <div>
        <section class="py-5" v-for="blog in featuredBlog" :key="blog.id">
                <div class="container px-5">
                    <h1 class="fw-bolder fs-5 mb-4">Popular Blog</h1>
                    <div class="card border-0 shadow rounded-3 overflow-hidden">
                        <div class="card-body p-0">
                            <div class="row gx-0">
                                <div class="col-lg-6 col-xl-5 py-lg-5">
                                    <div class="p-4 p-md-5">
                                        <div class="badge bg-primary bg-gradient rounded-pill mb-2">News</div>
                                        <div class="h2 fw-bolder">{{blog.blog_title}}</div>
                                        <p>{{blog.blog_short_description}}</p>
                                        <a class="stretched-link text-decoration-none" href="#!">
                                            Read more
                                            <i class="bi bi-arrow-right"></i>
                                        </a>
                                    </div>
                                </div>
                                <div class="col-lg-6 col-xl-7"><img class="bg-featured-blog" :src="'http://localhost/laravel-blog-project/public/'+blog.blog_image" width="100px" height="100px"/></div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
    </div>
</template>

<script>
export default {
  name: 'VueRestApiBlogProjectHomefeaturedblog',

  data () {
    return {
      featuredBlog: []
    }
  },

  mounted () {

  },

  methods: {
    showFeaturedBlog: function () {
      this.$http.get('http://localhost/laravel-blog-project/public/api/latest-blog')
        .then(function (response) {
          this.featuredBlog = response.body
        })
    }
  },

  created () {
    this.showFeaturedBlog()
  }
}
</script>

<style scoped>

</style>
