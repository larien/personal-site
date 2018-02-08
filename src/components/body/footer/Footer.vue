<template>
  <div class="footer-font footer-center">
      <footer>
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
        font-size: 2em;
    }

    .footer-center {
        position: fixed;
        padding-bottom: 1%;
        left: 0;
        bottom: 0;
        width: 100%;
        text-align: center;
    }
</style>