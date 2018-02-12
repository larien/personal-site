<template>
  <div class="l-body">
    <l-navigation-bar class="l-header light-gray-font"></l-navigation-bar>
    <l-content class=" l-content light-white-font"></l-content>
    <l-footer class="l-footer light-gray-font"></l-footer>
  </div>
</template>

<script>
import Content from './content/Content.vue';
import Footer from './footer/Footer.vue';
import NavigationBar from './navigation-bar/NavigationBar.vue';

export default {
  components: {
    'l-content': Content,
    'l-footer': Footer,
    'l-navigation-bar': NavigationBar
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

    .l-body {
      display: grid;
      grid-template-rows: 10vh auto 10vh;
      height: 100vh;
    }

    .l-header {
      grid-column: 1 / -1;
      overflow:auto;
      height: 100%;
    }

    .l-content {
      height: 80%;
    }

    .l-footer {
      display: grid;
      grid-column: 1 / -1;
      overflow:auto;
      height: 100%;
    }

@media (max-width: 700px) 
{
  .l-content{
    padding: 10%;
  }
}


</style>
