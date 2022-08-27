<template>
  <h1>这是App的根组件</h1>
  <hr>
<!--  使用todoList组件-->
  <TodoList.vue>fdgdgds</TodoList.vue>
</template>

<script>
  import TodoList from "./components/todo-list/TodoList.vue"
  export default {
    name: 'MyApp',
    components: {TodoList},
    data(){
      return{

      }
    },
    methods: {
      addCount(){
        this.count++;
      }
    }
  }
</script>

<style lang="css" scoped>
  h1{
    color: #f5083b;
  }
  .title{
    color: #ffffff;
  }

</style>
