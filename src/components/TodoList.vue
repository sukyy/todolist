<template>
  <ul class="todo-main">
    <TodoItem v-for="(todo, index) in todos" :key="index"
              :todo="todo" :deleteTodo="deleteTodo" :index="index"/>
  </ul>
</template>

<script>
  import TodoItem from './TodoItem.vue'
  export default {
    // 声明接收标签属性
    props: ['todos', 'deleteTodo'], 

    components: {
      TodoItem
    }
  }
</script>

<style>
  .todo-main {
    margin-left: 0px;
    border: 1px solid rgb(224, 183, 183);
    border-radius: 2px;
    padding: 0px;
  }

  .todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
  }
</style>