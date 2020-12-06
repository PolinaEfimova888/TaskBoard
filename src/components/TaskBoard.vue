<template>
    <div> 
     <ul>
    <TaskBoardComp
    v-for="(todo, i) of todos" :key="todo.id"
    v-bind:todo="todo"
    v-bind:index="i"
    v-on:remove-todo="removeTodo"
    
    />

     </ul>

    </div>
</template>


<script>
import TaskBoardComp from '@/components/TaskBoardComp'
export default {
    props: ['todos'],
  components: {
    TaskBoardComp
  },
  methods:{
    removeTodo(id){
      this.$emit('remove-todo', id)
 

    }
  }
}

</script>

<style scoped>

ul{
  list-style:none;
  margim:0;
  padding:0;
}
</style>