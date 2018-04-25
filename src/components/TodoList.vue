<template>
  <div>
    <text>TODOLIST</text>
    <textarea v-model="newtodo"></textarea>
    <button @click="addTodo">ADD TODO</button>
    <list class="todolist">
      <cell v-for="todo in todos">
        <div>
          <text>{{todo}}</text>
        </div>
      </cell>
    </list>
  </div>
</template>

<script>
export default {
  name: 'TodoList.vue',
  data () {
    return {
      newtodo: '',
      todos: ['aa', 'bb']
    }
  },
  methods: {
    addTodo () {
      this.todos.push(this.newtodo)
    }
  }
}
</script>

<style scoped>
  .todolist {
    width: 400px;
    height: 400px;
  }
  cell div {
    width: 200px;
    height: 100px;
  }
</style>
