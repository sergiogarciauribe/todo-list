<template>
  <div id="app">
    <ul class="todo-list">
      <li class="title">
        <b>Lista de tareas</b>
        <div>
          <input type="text"></div>
      </li>
      <li v-for-="task in tasks" :class="{'complete':task.selected}">
        <input type="checkbox" v-model="task.selected"/>
        {{task.name}}
      </li>
    </ul>
  </div>
</template>

<script>


export default {
  name: 'App',
   data: {
     tasks: [
       {name : "Ir a clase de programación Web 1", selected: false},
       {name : "Ir a clase de programación Web 1", selected: false},
       {name : "Ir a clase de programación Web 1", selected: false},
     ]
   },
  components: {
  },
};
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
.todo-list{
  padding: 20px;
  border: 1px solid gray;
  border-radius: 10px;
  margin: 10px auto;
  width: 400px;
  .title{
    margin-bottom: 5px;
  }
  .complete{
    text-decoration: line-through;
  }
}
</style>
