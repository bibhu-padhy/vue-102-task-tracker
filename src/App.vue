<template>
  <div class="main_container">
    <Header title="Task Tracker!" />
    <Tasks
      @double-click="doubleClicked"
      @delete-task="deleteTask"
      v-bind:tasksArr="tasks"
    />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Tasks from "./components/Tasks.vue";
export default {
  name: "App",
  components: {
    Header,
    Tasks,
  },
  methods: {
    doubleClicked(id) {
      this.tasks = this.tasks.map(task=>{})
    },
    deleteTask(id) {
      console.log(id);
    },
  },
  data() {
    return {
      tasks: [],
    };
  },
  created() {
    this.tasks = [
      {
        id: 1,
        text: "Doctors Appointment",
        day: "March 1st at 2:30",
        reminder: false,
      },
      {
        id: 2,
        text: "Doctors Appointment",
        day: "March 1st at 2:30",
        reminder: true,
      },
      {
        id: 3,
        text: "Doctors Appointment",
        day: "March 1st at 2:30",
        reminder: true,
      },
      {
        id: 4,
        text: "Doctors Appointment",
        day: "March 1st at 2:30",
        reminder: true,
      },
    ];
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.main_container {
  margin: auto;
  width: 500px;
  min-height: 400px;
  border: 1px solid saddlebrown;
  padding: 10px;
}
</style>
