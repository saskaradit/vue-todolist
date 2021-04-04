<template>
  <header>
    <h1>{{title}}</h1>
    <Button :text="showAddTask ? 'Close' : 'Add Task'" :color="showAddTask? 'red': 'teal' " @btn-click="$emit('toggle-form')"/>
  </header>
</template>

<script>
  import Button from './Button'

  export default {
    name: 'Header',
    props: {
      title: {
        type: String,
        default: "Hello World"
      },
      showAddTask: Boolean
    },
    components: {
      Button
    }
  }
</script>

<style scoped>
  header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
  }
</style>