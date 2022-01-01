<template>
  <header>
      <h4>{{title}}</h4>
 
  </header>
</template>

<script>

export default {
       name:'Header',
       props:['title','app'],
       components:{
           
       }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>