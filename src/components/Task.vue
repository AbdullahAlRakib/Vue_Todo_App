<template>
<div :class="[task.reminder ? 'reminder':'','task']">
     <h3>{{ task.text }} 
         <i @click="onDelete(task.id)" class="far fa-trash-alt"></i>
         
    </h3>
     <p>{{ task.day }}</p>
</div>
   
</template>
<script>
export default{
    name:'Task',
    props:{
        task:Object
    },
    methods:{
        onDelete(id){
          this.$emit('delete-task',id)
        }
    }

}
</script>
<style  scoped>
.far {
  color: red;
}
.task {
  background: #f3d8d8;
    margin: 5px;
    padding: 5px 13px;
    cursor: pointer;
}
.task.reminder {
  border-left: 3px solid #bd27fb;;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
