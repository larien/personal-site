<template>
  <div id="l-body">
    
    <l-content></l-content>
  
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

#l-body {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
