<template>
<div>
  <prograss></prograss> 
  <div class="row">
  </div>
   
</div>

</template>

<script>
import prograss from './components/Prograssbar.vue';

export default {

components:{
  Prograss:prograss,
}
}
</script>

<style scoped>
div{
  max-width: 90%;
  margin:0 auto;
}
</style>
