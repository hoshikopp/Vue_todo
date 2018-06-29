<template>
<body>
  <section class="section">
    <AddForm @add-task='addTask' v-bind:test="tasks"/>
    <div class="container">
    </div>
  </section>
  </body>
</template>

<script>
import AddForm from './components/AddForm.vue'
export default {
  name: 'app',
  components: {
    AddForm
  },
  data: function() {
    return {
      tasks: []
    }
  },
  methods: {
    addTask: function(text) {
      this.tasks.push(text)
    }
  }
}
</script>

<style>
@import "../node_modules/bulma/bulma.sass";

</style>
