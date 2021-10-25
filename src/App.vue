<template>
  <div id="app">
    <main class="flex-shrink-0">
            <!-- Navigation-->
            <MyHeader/>
            <!-- Page Content-->
            <router-view/>
        </main>
        <!-- Footer-->
        <MyFooter/>
  </div>
</template>

<script>
import Header from './components/includes/Header'
import Footer from './components/includes/Footer'

export default {
  name: 'App',
  components: {
    'MyHeader': Header,
    'MyFooter': Footer
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
