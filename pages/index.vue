<template>
  <div
    class="app-overlord relative bg-slate-800 w-full flex justify-center overflow-hidden"
  >
    <div
      class="main-container relative bg-slate-700 border-2 rounded w-80 h-4/5 m-auto p-8 flex flex-col"
    >
      <transition name="modal">
        <template v-if="isModalOpen">
          <div
            id="create_modal"
            class="todo-create-modal absolute bg-slate-300 left-full h-full w-full bg-slate-200"
          >
            <!-- ? Search how to left 100% when isModalOpen goes active. This can only happen after the component is loaded -->
            <!-- ? Modal goes off to the right then on create click bring the modal inwards. -->
          </div>
        </template>
      </transition>
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
        @click="toggleModal"
      >
        Create
      </button>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isModalOpen: false,
      newTodo: "",
      todos: [],
    };
  },
  methods: {
    //Toggle Modal
    toggleModal() {
      this.isModalOpen = !this.isModalOpen;
      console.log(this.isModalOpen);
    },
    //Create
    createTodo() {},
    //Delete
    deleteTodo() {},
    //Done
    checkTodo() {},
  },
};
</script>
