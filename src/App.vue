<template>
<body>
  <section class="section">
    <AddForm @add-task='addTask'/>
    <ul>
      <TodoList v-for='(task, index) in tasks' v-bind:task='{ task: task, index: index }'/>
    </ul>
    <div class="container">
    </div>
  </section>
  </body>
</template>

<script>
import AddForm from './components/AddForm.vue'
import TodoList from './components/TodoList.vue'

export default {
  name: 'app',
  components: {
    AddForm,
    TodoList
  },
  data: function() {
    return {
      tasks: []
    }
  },
  methods: {
    addTask: function(text) {
      this.tasks.push(text)
    },
    deleteTask: function(index) {
      this.todos.splice(index, 1)
    }
  }
}
</script>

<style>
@import "../node_modules/bulma/bulma.sass";

</style>
