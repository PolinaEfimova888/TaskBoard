<template>

 <div>

  <Header/>
  <AfterHeader/>

  <AddTask
    @add-todo="addTodo"
  
  />
  <TaskBoard

    v-bind:todos="todos"
    @remove-todo="removeTodo"

  
  />


 </div>


</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import TaskBoard from '@/components/TaskBoard'
import Header from '@/components/Header'
import AddTask from '@/components/AddTask'
import AfterHeader from '@/components/AfterHeader'

export default {
  name: 'App',
  data(){
    return{
      todos: [
        {id:1, title: 'To stop your minds', completed: false},
        {id:2, title: 'To break your minds', completed:false},
        {id:3, title: 'To open your minds', completed:false}
      ]
    }
  },
  methods:{
removeTodo(id){
  this.todos = this.todos.filter(t=>t.id !==id)
},
addTodo(todo){
  this.todos.push(todo)
}

  },

  components: {
    TaskBoard,
    Header, AddTask,  AfterHeader
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

}
h1 {
    text-align:  center;
   }
</style>
