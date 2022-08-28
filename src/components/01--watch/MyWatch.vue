<template>
   <div>
     <input type="text" class="form-control" v-model="userName"/>
   </div>
</template>

<script>
export default {
  name: "MyWatch",
  data(){
    return{
      userName : ''
    }
  },
  watch: {
    userName(newValue,oldValue){
      console.log(newValue,'newValue');
      console.log(oldValue,'oldValue')
    }
  }
}
</script>

<style scoped>

</style>
