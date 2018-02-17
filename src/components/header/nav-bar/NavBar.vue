<template>
  <div id="l-nav-bar" class="light-white-font">

    <l-language-switch classes="is-warning" v-model="value" checked>{{text}}</l-language-switch>

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
    #l-nav-bar {
        font: {
            family: 'Coda', 'Arial', monospace;
        }
    }    
</style>