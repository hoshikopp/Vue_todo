<template>
    <li>
      {{ task.task }}
      <a class="button" v-on:click="deleteTask">削除</a>
    </li>
</template>

<script>
export default{
  name: 'todoList',
  props: [
    'task'
  ],
  methods: {
    deleteTask: function() {
      this.$emit('deleteTodo', this.task.index )
    }
  }
}
</script>

<style lang="scss">
@import "../../node_modules/bulma/bulma.sass";

</style>

現状はtodosは文字列なので、オブジェクトの配列にする
trueかfalseにして、
todosをオブジェクトにする