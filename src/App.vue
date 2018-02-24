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

.l-header {
  height: 70px;
  flex-shrink: 0;
}

#l-app {
  min-height: 360;
  height: 100vh;
  display: flex;
  flex-direction: column;
}

.l-body {
  flex: auto 1 0;
  margin: 0px 10px 76px 10px;
}

.l-footer {
  height: 76px;
  position:absolute;
  bottom:0;
}

@media (min-width: 600px) {
  #l-app {
    height: calc(100%-100px);
    display: flex;
    flex-direction: column;
  }
  .l-body {
    margin: 0px 10px 56px 10px;
  }

  .l-header {
    height: 50px;
  }

  .l-footer {
    height: 56px;
  }
}

@media (min-width: 1000px) {
  #l-app {
    height: calc(100vh-100px);
    display: flex;
    flex-direction: column;
  }
}
</style>
