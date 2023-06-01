<template>
  <div>
      <task-item @click="()=>handClickItem(index)" ref="item" @removeTask="removeTaik" v-for="(item, index) in taskList" :key="index" :task="item"></task-item>
  </div>
</template>

<script>
import  TaskItem from './TaikItem.vue'
export default {
   name:'TaikView',
   components:{
      TaskItem
   },
   data(){
       return {
           title:'hello',
           taskList:[
               {   
                   id:1,
                   name:'张三'
               },
               {   
                   id:2,
                   name:'李四'
               }
           ]
       }
   },
   methods:{
    removeTaik(id){
        this.taskList=this.taskList.filter(item=>item.id!==id)
    },
    getTaik(){
        alert(this.title)
    },

    handClickItem(index){
        console.log(index);
        // this.$refs.item
    }
   }
}
</script>

<style>

</style>