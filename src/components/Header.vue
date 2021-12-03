<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      @click="$emit('toggle-add-task')"
      :text="isAddTask ? 'Close' : 'Add Task'"
      :color="isAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  props: {
    title: String,
    isAddTask: Boolean,
  },
  components: {
    Button,
  },
  emits: ["toggle-add-task"],
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
