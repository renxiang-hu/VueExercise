<template>
  <h1>这是App的根组件</h1>
  <hr>
  <TodoInput @add="onAddNewTask"></TodoInput>
  <TodoList :todoList="todoList" class="mt-2"></TodoList>
  <todoButton :active="activeBtnIndex"></todoButton>
</template>

<script>
  import TodoList from "./components/todo-list/TodoList.vue"
  import TodoInput from "./components/todo-input/TodoInput.vue";
  import TodoButton from "./components/todo-button/TodoButton.vue";

  export default {
    name: 'MyApp',
    components: {TodoButton, TodoInput, TodoList},
    data(){
      return{
       activeBtnIndex:1,
        //任务列表数据
       todoList:[
         {id:1,task:'周一早晨9点开会',done:false},
         {id:2,task:'周一晚上8店聚餐',done:false},
         {id:3,task:'准备周三上午的演讲稿',done: true}
       ],
        nextId:4
      }
    },
    methods: {
      onAddNewTask(taskName){
        this.todoList.push({
          id:this.nextId,
          task: taskName,
          done: false
        });
        this.nextId++;
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
