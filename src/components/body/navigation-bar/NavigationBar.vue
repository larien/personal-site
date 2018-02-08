<template>
  <div class="navigation-bar-center navigation-bar-font light-gray-font">
      <header>
          <!-- <p><l-language-switch></l-language-switch></p> -->
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

<style scoped lang="scss">
    .navigation-bar-font {
        font: {
            family: 'Coda', 'Arial', monospace;
            size: 0.5em;
        }
    }    

    .navigation-bar-center {
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 10%;
    }
</style>