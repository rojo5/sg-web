<template>
  <div>
    <Navbar />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import Footer from '~/components/common/Footer.vue'
import  Navbar from '~/components/common/Navbar.vue'

export default {
  components:{Navbar, Footer}

}
</script>


<style>
</style>
