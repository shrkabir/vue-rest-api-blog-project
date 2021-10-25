<template>
  <div id="app">
    <main class="flex-shrink-0">
        <!-- Navigation-->
        <my-header/>
        <!-- Page Content-->
        <router-view/>
    </main>
        <!-- Footer-->
        <my-footer/>
  </div>
</template>

<script>
import Header from './components/includes/Header'
import Footer from './components/includes/Footer'

export default {
  name: 'App',
  components: {
    'my-header': Header,
    'my-footer': Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
