<template>
    <div
    :class="['item', ItemProps && ItemProps.status ? 'is-completed' : '']"    >
      <div class="content">
        <input type="checkbox" 
          :checked="ItemProps.status" 
          @change="choiceItem"
        />
  
        <h1>{{ ItemProps.title }}</h1>
      </div>
  
      <button @click="deleteItem">Delete</button>
    </div>
  </template>
  
  <script>
  export default {
    name: "TodoItem",
    props: ["ItemProps"],
    setup(props, context) {
      const choiceItem = () => {
        context.emit('itemCompleted', props.ItemProps.id);
      };
  
      const deleteItem = () => {
        // Thêm logic để xóa mục dựa vào props.ItemProps.id
        console.log('Delete button clicked');
      };
  
      return {
        choiceItem,
        deleteItem
      };
    },
  };
  </script>
  
  <style>
  /* ... */
  </style>
  