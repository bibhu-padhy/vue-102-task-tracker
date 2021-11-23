<template>
  <div
    @dblclick="doubleClicked(task.id)"
    :class="[task.reminder ? 'reminder' : '', 'task_container']"
    v-for="(task,index) in tasksArr"
    v-bind:key="index"
  >
    <div class="task_text">
      {{ task.text }}
      <div @click="$emit('delete-task', task.id)">x</div>
    </div>
    <div class="task_day">{{ task.day }}</div>
  </div>
</template>

<script>
export default {
  name: "Tasks",
  props: {
    tasksArr: [],
  },
  methods: {
    doubleClicked(id) {
      this.$emit("double-click", id);
    },
  },
  emits: ["double-click", "delete-task"],
};
</script>

<style scoped>
.task_container {
  border: 1px solid gray;
  padding: 0 10px;
  margin-bottom: 10px;
  cursor: pointer;
}
.task_text {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.task_day {
  font-size: 0.8rem;
}
.reminder {
  border-left: 3px solid green;
}
</style>
