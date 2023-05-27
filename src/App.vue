<template>
  <div>
    <FormTodo @save="insertTodo"/>
    <ToDolist :todos="todos"/>
</div>
</template>


<script>
import FormTodo from './components/FormTodo.vue'
import ToDolist from './components/ToDolist.vue';

export default {
  name:"App",
  components:{
    FormTodo,ToDolist
  },
  data(){
    return{
        todos:[]
    }
  },
  methods:{
    insertTodo(data){
      this.todos.push(data);
    },
  }
}
</script>

<style>
 
</style>