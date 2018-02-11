<template>
  <div class="footer-center">
      <footer class="footer-font">
          <l-contact></l-contact>
        </footer>
  </div>
</template>


<script>
import Contact from './contact/Contact.vue';
export default {
  components: {
      'l-contact': Contact
  }
}
</script>

<style scoped>
    .footer-font {
        font-family: 'Coda', 'Arial', monospace;
    }

    .footer-center {

    }
</style>