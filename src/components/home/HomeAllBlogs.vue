<template>
    <div>
        <section class="py-5">
                <div class="container px-5">
                    <h2 class="fw-bolder fs-5 mb-4">Featured Stories</h2>
                    <div class="row gx-5">
                        <div class="col-lg-4 mb-5" v-for="Blog in allBlogs" :key="Blog.id">
                            <div class="card h-100 shadow border-0">
                                <img class="card-img-top" :src="'http://localhost/laravel-blog-project/public/'+Blog.blog_image" alt="..." />
                                <div class="card-body p-4">
                                    <div class="badge bg-primary bg-gradient rounded-pill mb-2">News</div>
                                    <a class="text-decoration-none link-dark stretched-link" href="#!"><div class="h5 card-title mb-3">{{Blog.blog_title}}</div></a>
                                    <p class="card-text mb-0">{{Blog.blog_short_description}}</p>
                                </div>
                                <a class="stretched-link text-decoration-none" href="#!">
                                            Read more
                                    <i class="bi bi-arrow-right"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="text-end mb-5 mb-xl-0">
                        <a class="text-decoration-none" href="#!">
                            More stories
                            <i class="bi bi-arrow-right"></i>
                        </a>
                    </div>
                </div>
            </section>
    </div>
</template>

<script>
export default {
  name: 'VueRestApiBlogProjectHomeallblogs',

  data () {
    return {
      allBlogs: []
    }
  },

  mounted () {

  },

  methods: {
    showAllBlogs: function () {
      this.$http.get('http://localhost/laravel-blog-project/public/api/all-blogs-api')
        .then(function (response) {
          this.allBlogs = response.body
        })
    }
  },

  created () {
    this.showAllBlogs()
  }
}
</script>

<style scoped>

</style>
