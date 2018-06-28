<template>
  <section class="section">
    <div class="field">
　   <div class="control">
      <input class="input is-danger" type="text" placeholder="Danger input" v-model= "tasks">
     </div>
　   </div>
    <input class="button" type="submit" value="追加" v-on:click= "$emit('tasks')">
      <p>{{ tasks }}</p>
  </section>
</template>

<script>
export default{
  data: function() {
    return {
      tasks: ""
    }
  }
}

</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";

</style>
