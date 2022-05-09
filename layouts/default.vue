<template>
  <div class="bg-black">
    <navbar />
    <Nuxt />
    <Footer />
  </div>
</template>
<script>

import Navbar from "../components/navbar.vue";
import Footer from "../components/footer.vue";
import Home from "~/pages/home.vue";
export default{
    name:'default',
    components: { Navbar, Footer, Home }
}
</script>