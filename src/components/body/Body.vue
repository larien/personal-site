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
.l-content {
  height: 80vh;
}

@media (max-width: 700px) 
{
  .l-content{
    padding-right: 10%;
    padding-left: 10%;
    height: auto;
  }
}

</style>
