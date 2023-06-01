<template>
  <div>
    <p>{{ task.name }}</p>
    <button @click="delTask">删除</button>
    <button @click="getTaik">获取父组件</button>
  </div>
</template>

<script>
export default {
  props: {
    task: {
      type: Object,
      required: true,
    },
  },
  methods: {
    delTask() {
      this.$emit("removeTask", this.task.id);
    },
    // 子组件调用方法
    getTaskName() {
      alert(this.task.name);
    },
    // 调用父组件的方法
    getTaik(){
        this.$parent.getTaik()
    },
  },
};
</script>

<style></style>
