<template>
  <div>
    <ol>
      <TodoItem v-for="todo in todos" :key="todo.id" :item="todo"></TodoItem>
    </ol>
  </div>
</template>

<script>
import TodoItem from '@/components/TodoItem'
export default {
  components: {
    TodoItem
  },
    beforeCreate() {
    console.log('beforeC')
  },
  created() {
    console.log('created')
  },
  beforeMount() {
    console.log('beforeM')
  },
  mounted() {
    console.log('mounte d')
  },
  beforeDestroy() {
    console.log('berfore destroy')
  },
  data() {
    return {
      todos: [
        { id: 1, text: 'Hello world' },
        { id: 2, text: 'Hello baby' },
        { id: 3, text: 'Hello god' }
      ]
    }
  }
}
</script>

<style></style>
