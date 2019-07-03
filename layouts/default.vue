<template>
  <div>
    <Header />
    <div class="main-content">
      <nuxt />
    </div>
    <Footer />
  </div>
</template>

<style lang="sass" scoped>
</style>

<script>
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Header,
    Footer
  }
};
</script>