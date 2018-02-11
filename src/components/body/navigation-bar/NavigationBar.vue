<template>
  <div class="navigation-bar-center navigation-bar-font light-gray-font">
      <header>
          <p><l-language-switch></l-language-switch></p>
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
        }
    }    

    .navigation-bar-center {

    }
</style>