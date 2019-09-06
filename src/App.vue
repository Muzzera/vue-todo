<template>
  <div id="app">
    <Todos 
      v-bind:todos="todos"
      v-on:del-todo="deleteTodo"
      />
  </div>
</template>

<script>

import Todos from "./components/Todos";
export default {
  name: 'app',
  components: {
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "delectus aut autem",
          completed: true
        },
        {
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false
        },
        {
          id: 3,
          title: "fugiat veniam minus",
          completed: false
        },
        {
          id: 4,
          title: "et porro tempora",
          completed: true
        },
        {
          id: 5,
          title: "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false
        },
        {
          id: 6,
          title: "qui ullam ratione quibusdam voluptatem quia omnis",
          completed: true
        },
        {
          id: 7,
          title: "illo expedita consequatur quia in",
          completed: false
        },
        {
          id: 8,
          title: "quo adipisci enim quam ut ab",
          completed: true
        }
      ]
    }
  },
  methods : {
    deleteTodo (id) {
      this.todos = this.todos.filter( todo => todo.id !== id );
    }
  }
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
  .btn {
    display: inline-block;
    border: none;
    background: #555;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }
  .btn:hover {
    background: #666;
  }
</style>
