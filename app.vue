<template>
  <div class="main-layout">
    <!-- <div class="sticky-header"> -->
      <Header />
    <!-- </div> -->
    <router-view/>
    <Footer />
    <ScrollToTopButton />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'
import ScrollToTopButton from '~/components/ScrollToTopButton.vue';
</script>

<style scoped>
.main-layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* .sticky-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
} */
</style>