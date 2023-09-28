<template>
  <div
    class="todo-item list-item bg-slate-200 w-full h-16 border-1 rounded items-center"
  >
    <h5>{{ todo }}</h5>
    <button type="button">Delete</button>
  </div>
</template>
<script>
export default {
  props: {
    todo: {
      type: Object,
      default: () => {},
    },
  },
};
</script>
