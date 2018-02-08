<template>
  <div class="navigation-bar-center navigation-bar-font light-gray-font">
      <header>
          <l-language-switch></l-language-switch>
        </header>
  </div>
</template>


<script>
import LanguageSwitch from './language-switch/LanguageSwitch.vue';

export default {
  components: {
      'l-language-switch': LanguageSwitch
  }
}
</script>

<style scoped>
    .navigation-bar-font {
        font-family: 'Coda', 'Arial', monospace;
        font-size: 0.5em;
    }

    .navigation-bar-center {
        position: fixed;
        padding-top: 1%;
        left: 0;
        top: 0;
        width: 95%;
        text-align: right;
    }
</style>