<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @btn-click="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
    <!-- <Button text="Update Task" color="blue" />
    <Button text="Delete Task" color="red" /> -->
  </header>
</template>

<script>
import Button from './Button.vue';
export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      default: 'Hello',
    },
    showAddTask: Boolean,
  },
  components: {
    Button,
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
