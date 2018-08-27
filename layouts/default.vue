<template>
  <div>
    <navbar/>
    <nuxt/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: {
    Navbar,
    Footer,
  }
}
</script>


<style>
  @import '../static/css/style.css';
  @import '../static/css/zerogrid.css';
  @import '../static/css/reset.css';
</style>

