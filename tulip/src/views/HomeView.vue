<template>
  <div class="home">
   <Header id="header"/>
   <Presentation id='company'/>
   <Process id="process"/>
   <Products id="products"/>
   <Contact id="contact"/>
   <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '../components/Header.vue';
import Presentation from '../components/Presentation.vue';
import Process from '../components/Process.vue';
import Products from '../components/Products.vue';
import Contact from '../components/Contact.vue';
import Footer from '../components/Footer.vue';
import Carousel from '../components/Carousel.vue'
import Navbar from '@/components/Navbar.vue';
export default {
  name: 'HomeView',
  components: {
    Header,
    Presentation,
    Products,
    Footer,
    Process,
    Contact,
    Carousel,
    Navbar
}
}
</script>
<style>
.home{
  /*min-height: 100vh;*/
  
}
</style>