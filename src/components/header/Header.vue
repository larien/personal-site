<template>
  <div id="l-header">

	<!-- <img src="resources/logo.svg"> -->
    <l-nav-bar class="switch"></l-nav-bar>

  </div>
</template>

<script>
import NavBar from './nav-bar/NavBar.vue';

export default {
  components: {
    'l-nav-bar': NavBar
  }
}
</script>

<style lang="scss">
    #l-header{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .switch{
        position: absolute;
        top: 15px;
        right: 10px;
    }

    @media (min-height: 600px) and (min-width: 800px){
        .switch{
            top: 10px;
        }
    }

    .logo img{
        display: block;
        width: 50px;
        height: 50px;
    }
</style>