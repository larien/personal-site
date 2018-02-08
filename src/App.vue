<template>
  <div class="primary-background-color" >

    <l-body></l-body>

  </div>
</template>

<script>
import Body from './components/body/Body.vue';

export default {
  components: {
    'l-body': Body
  }
}
</script>

<style lang="scss">
html {
    background-color: #1B2836;
}
</style>
