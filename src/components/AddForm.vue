<template>
  <section class="section">
    <div class="field">
　   <div class="control">
      <input class="input is-danger" type="text" placeholder="Danger input" v-model="task">
     </div>
　   </div>
    <input class="button" type="submit" value="追加" v-on:click="addTask">

  </section>
</template>

<script>
export default{
  data: function() {
    return {
      task: ""
    }
  },
  methods: {
    addTask: function() {
      this.$emit('add-task', this.task)
    }
  }
}

</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";

</style>
