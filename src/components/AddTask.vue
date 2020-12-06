<template>

<b-container>

  <form @submit.prevent="onSubmit" class="p-3">   
     
    
      <b-input-group prepend="" class="mt-3">
        <b-form-input type="text" v-model="title" placeholder="to change my life"></b-form-input>
          <b-input-group-append>
          <b-button type="submit" variant="info">Create</b-button>
        </b-input-group-append>
       </b-input-group>   
  
   </form>
   

</b-container>
    
</template>

<script>
export default {
  data(){
    return{
      title:''
    }
  },
  methods:{
    onSubmit(){     
      if (this.title.trim()) {
        const newTodo = {
          id: Date.now(),
          title:this.title,
          completed: false
        }

        this.$emit('add-todo', newTodo)
        this.title =''

      }
    

    }
  }
  
}
</script>


<style scoped >

.b-container{
  margin: auto;

}
input{
  width:400px;

}
.p-3 {
  padding: $spacer !important;
}
</style>
