<template>
  <div class='divContainer'>
    <list-tasks :tasks="tasks" />
    <btn-add v-bind:onClick="newTask" color="red" />
    <modal-new-task v-bind:save="save" title="New Task" v-bind:showDialog="dialog" v-bind:task="task" />
  </div>
</template>

<script>
import BtnAdd from "../components/ButtonPlus.vue";
import ModalNewTask from "../components/ModalNewTask.vue";
import ListTasks from '../components/ListTasks.vue';

export default {
  data() {
    return {
      dialog: false,
      task: {},
      tasks: [],
      
    };
  },
  components: {
    BtnAdd,
    ModalNewTask,
    ListTasks,
  },
  methods: {
    newTask() {
       this.dialog = true
    },
    save() {
      console.log(this.task)
      this.tasks.push(this.task);
      this.task = {};
      this.dialog = false;
    },
  },
};
</script>

<style>
.divContainer{
  flex: 1;
  flex-direction: column;
  align-items: center;
  justify-content:center;
  margin:0px auto 10px auto;
  max-width: 700px;
}
</style>