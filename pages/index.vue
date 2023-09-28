<template>
  <div class="app-overlord bg-slate-800 w-full flex justify-center">
    <div
      class="bg-slate-700 border-2 rounded w-80 h-4/5 m-auto p-8 flex flex-col"
    >
      <h2
        class="w-full flex justify-center text-xl text-white font-mono grow-0"
      >
        Todo List
      </h2>
      <div class="list-container w-full grow">
        <template>
          <todo-item :todos="todos"></todo-item>
        </template>
      </div>
      <button
        class="button relative bg-slate-400 border-1 rounded h-8 w-full grow-0 text-slate-200"
        type="button"
      >
        Create
      </button>
    </div>

    <div id="create_modal" class="todo-create-modal">
      <!-- ? Modal goes off to the right then on create click bring the modal inwards. -->
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      newTodo: "",
      todos: [],
    };
  },
  methods: {
    //Create
    createTodo() {},
    //Delete
    deleteTodo() {},
    //Done
    checkTodo() {},
  },
};
</script>
