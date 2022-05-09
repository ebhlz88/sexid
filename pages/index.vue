<template>
<div class="min-h-screen bg-black">
  <Navbar/>
  <Home to="home"></Home>
  <Footer class="relative w-full "></Footer>
</div>


</template>

<script>
import Navbar from "../layouts/navbar.vue";
import Footer from "../layouts/footer.vue";
import Home from "./home.vue";
export default {
    name: "IndexPage",
    components: { Navbar, Footer, Home }
}
</script>
