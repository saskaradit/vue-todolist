<template>
  <div :class="[task.reminder? 'reminder': '','task']" @dblclick="$emit('toggle-reminder',task.id)">
    <h3>
      {{task.text}}
      <p @click="$emit('delete-task',task.id)" class="fas">Delete</p>
    </h3>
    <p>{{task.day}}</p>
  </div>
</template>

<script>
  export default {
    name: 'Task',
    props: {
      task: Object
    },
  }
</script>

<style scoped>
.task{
  background: #f4f4f4;
  margin: 0.5rem;
  padding: 10px 20px;
  cursor: pointer;
}

.task.reminder {
  border-left: 5px solid teal;
}
.task h3{
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.fas{
  color: red;
}
</style>