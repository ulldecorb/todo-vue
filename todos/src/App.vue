<template>
  <div>
    <div id="header"></div>

    <div id="main-container">
      <h2>TODOS</h2>
      <Todos v-bind:todoslist="copyTodos" />
    </div>    
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld';
// import Search from './components/Search';
import Todos from './components/Todos';
// import TodoAdd from './components/TodoAdd';

export default {
  name: 'App',
  components: {
    Todos
  },
  data(){
    return {
      todos: [
        {
          id: 0,
          title: 'Create my first VUE App',
          complete: false
        },
        {
          id: 1,
          title: 'Test VUE App',
          complete: false
        },
        {
          id: 2,
          title: 'Enjoy afternoon',
          complete: false
        },
      ],
      copyTodos: []
    }
  },
  created(){
    this.copyTodos = [...this.todos];
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1.5em;
  padding: 0;
  margin: 0;
}

#main-container {
  border: solid 1px #ccc;
  width: 600px;
  margin: 100px auto;
}

#header {
  background: #000;
  padding: 10px;
}

h2 {
  padding: 0 10px;
}
</style>
