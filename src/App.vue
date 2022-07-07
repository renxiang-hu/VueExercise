<template>
  <h1>这是App的根组件</h1>
  <h2>{{username}}</h2>
  <h3 class="title">这是vue的组件</h3>
  <button @click="addCount">{{this.count}}</button>
</template>

<script>
  export default {
    name: 'MyApp',
    data(){
      return{
        username: 'hurenxiang',
        count:0
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
    color: blue;
  }

</style>
