<template>
  <div id="l-app">

    <l-header class="l-header"></l-header>
    <l-body class="l-body"></l-body>
    <l-footer class="l-footer"></l-footer>

  </div>
</template>

<script>
import Header from './components/header/Header.vue';
import Body from './components/body/Body.vue';
import Footer from './components/footer/Footer.vue';

export default {
  components: {
    'l-header': Header,
    'l-body': Body,
    'l-footer': Footer
  }
}
</script>

<style lang="scss">
.light-white-font {
    color: #FFFFFA;
}

.light-gray-font {
    color: #808F9A;
}

.middle-blue-font {
    color: #1DA1EB;
}

html {
    background-color: #1B2836;
}

.l-body {
  display: grid;
  grid-template-rows: 50px auto 50px;
  height: 100vh;
}
.l-header {
  grid-column: 1 / -1;
  overflow:auto;
  height: 100%;
}
.l-footer {
  display: grid;
  grid-column: 1 / -1;
  overflow:auto;
  height: 100%;
  position: relative;
}
</style>
