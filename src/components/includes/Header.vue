<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
                <div class="container px-5">
                    <a class="navbar-brand" href="index.html">My Blog</a>
                    <div class="collapse navbar-collapse" id="navbarSupportedContent">
                        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                            <li class="nav-item" v-for="category in categories" :key="category.id">
                                <a class="nav-link" href="index.html">{{category.category_name}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </nav>
    </div>
</template>

<script>
export default {
  name: 'VueRestApiBlogProjectHeader',

  data () {
    return {
      categories: []
    }
  },

  mounted () {

  },

  methods: {
    allPublishedCategories: function () {
      this.$http.get('http://localhost/laravel-blog-project/public/api/categories/published-categories')
        .then(function (response) {
          this.categories = response.body
        })
    }
  },

  created () {
    this.allPublishedCategories()
  }
}
</script>

<style scoped>

</style>
