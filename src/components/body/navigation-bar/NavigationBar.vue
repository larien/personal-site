<template>
  <div class="navigation-bar-center navigation-bar-font light-gray-font">
      <header>
          <p><l-language-switch classes="is-warning" v-model="value" checked>{{text}}</l-language-switch></p>
        </header>
  </div>
</template>


<script>
import LanguageSwitch from './language-switch/LanguageSwitch.vue';
import EventBus from '../../../eventbus.js';

export default {
  components: {
      'l-language-switch': LanguageSwitch
  },
    data() {
      return {
          value: false,
          text: 'EN'
      }
  },
  watch: {
      value(val) {
          this.text = val ? 'BR' : 'EN'
          this.emitMethod()
      }
  },
  methods: {
    emitMethod() {
       EventBus.$emit('change_language');
    }
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
        display: flex;
        justify-content: center;
        flex-direction: column;
        text-align: right;
        margin-right: -30px;
    }

</style>