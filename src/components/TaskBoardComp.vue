<template>

    <li> 
     <div class="a">
        <span v-bind:class="{done: todo.completed}">
            <input type="checkbox" v-on:change="todo.completed=!todo.completed">
            <strong>{{index+1}}</strong>
             {{todo.title}}
                <center>
                    <b-form-rating class="layer" variant="info" id="rating-inline" inline value="0"></b-form-rating>
                </center>
        </span>
     </div>

    <div class="b">
        <b-button pill variant="info" v-on:click="$emit('remove-todo', todo.id)" 
     >&times;</b-button>
     </div>
    </li>
     


</template>

<script>
export default {
    props:{
        todo:{
            type:Object,
            required:true
        },
        index: Number

    } 
}


</script>

<style scoped>

li{
  border:1px solid #ccc;

  justify-content:space-between;
  padding: .5rem 2rem;
  margin-bottom: 1rem;
}
.a{

  display:flex;

}
.b{

  margin-left:98%;

}

.done{
    text-decoration: line-through;
}
input{
    margin-right:1rem;
}

.layer {
    margin-left: 20%;}
</style>