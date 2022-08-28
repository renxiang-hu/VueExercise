<template>
   <div class="button-container mt-3">
     <div class="btn-group">
       <button type="button" class="btn" :class="active === 0 ? 'btn-primary' : 'btn-secondary'" @click="onBtnClick(0)">全部</button>
       <button type="button" class="btn" :class="active === 1 ? 'btn-primary' : 'btn-secondary'" @click="onBtnClick(1)">已完成</button>
       <button type="button" class="btn" :class="active === 2 ? 'btn-primary' : 'btn-secondary'" @click="onBtnClick(2)">未完成</button>
     </div>
   </div>
</template>

<script>
export default {
  name: "TodoButton",
  methods:{

  },
  props:{
    active:{
      type: Number,
      required: true,
      default: 0
    }
  }
}
</script>

<style scoped>
.button-container{
  width: 400px;
  text-align: center;
}
</style>
