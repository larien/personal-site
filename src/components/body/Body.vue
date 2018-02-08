<template>
  <div id="l-body">

    <l-footer class="light-gray-font"></l-footer>
    <l-content class="light-white-font"></l-content>
    <l-navigation-bar class="light-gray-font"></l-navigation-bar>
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

</style>
