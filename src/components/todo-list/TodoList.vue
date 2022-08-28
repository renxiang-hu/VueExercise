<template>
   <ul class="list-group">
     <li class="list-group-item d-flex justify-content-between align-items-center" v-for="item in todoList" :key="item.id">
       <div class="custom-control custom-checkbox">
          <input type="checkbox" class="custom-control-input" :id="item.id" v-model="item.done"/>
          <label class="custom-control-label" :class="item.done ? 'delete' : ''" :for="item.id">{{item.task}}</label>
       </div>
       <span class="badge badge-success badge-pill" v-if="item.done">完成</span>
       <span class="badge badge-warning badge-pill" v-else>未完成</span>
     </li>
   </ul>
</template>

<script>
export default {
  name: "TodoList.vue",
  props: {
    todoList:{
      type:Array,
      required:true,
      default:[]
    }
  }
}
</script>

<style scoped>
.list-group{
  width: 600px;
}
.delete{
  text-decoration: line-through;
  color: gray;
  font-style: italic;
}
</style>
