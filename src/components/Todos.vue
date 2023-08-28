<template>
  <TodoItem 
  v-for="todo in todos" 
  v-bind:key="todo" 
  v-bind:ItemProps = "todo" 
  v-on:itemCompleted = "choiceCheckBox"
  /> 
</template>

<script>
import { ref } from "vue";
import TodoItem from "./TodoItem.vue";


export default {
  name: "Todos",

  components:{ 
    TodoItem 
  },

  setup() {
    const todos = ref([
      { id:1,title: 'Viec 1',status: true},
      { id:2,title: 'Viec 2',status: false},
      { id:3,title: 'Viec 3',status: false},
    ]);

    const choiceCheckBox = id =>{
      console.log(30,id);
      todos.value = todos.value.map(todo=>{
        if(todo.id === id){
          return todo.status = !todo.status
        }
      })
    }

    return {
      todos,
      choiceCheckBox   
    };
  },
};
</script>

<style>
</style>