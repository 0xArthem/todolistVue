<template>
  <TodoList/>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'App',
  components: {
    TodoList
}
}
</script>

<style>
#app {
  margin: 60px;
  text-align:center;
}
</style>
