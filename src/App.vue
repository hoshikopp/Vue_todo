<template>
<body>
  <section class="section">
    <AddForm/>
    <div class="container">
      <h1 class="title">
        {{ tasks }}
      </h1>
      <p class="subtitle">
        My first website with <strong>Bulma</strong>!
        <add-form v-model= "tasks" @tasks= "addTask"></add-form>
      </p>
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
      this.tasks = text
    }
  }
}
</script>

<style>
@import "../node_modules/bulma/bulma.sass";

</style>
