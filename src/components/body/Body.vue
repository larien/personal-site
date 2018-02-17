<template>
  <div id="l-body">
    
    <l-content class="l-content light-white-font"></l-content>
  
  </div>
</template>

<script>
import Content from './content/Content.vue';

export default {
  components: {
    'l-content': Content
  }
}
</script>

<style lang="scss">

.l-body {
  // background-color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
