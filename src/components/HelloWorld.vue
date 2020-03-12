<template>
  <div class="w-full max-w-xs text-center mx-auto">
    <form @submit.prevent="addTask" class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
      <h1 class="highlight-title p-4">WOLF TODO</h1>
      <input class="shadow appearance-none border rounded py-2 px-3 text-gray-700 leading-tight text-center" type="text" v-model="task" name="task" placeholder="Add Task"/>
      <button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded inline-flex items-center" type="submit">Add Task</button>
      <h1 class="p-4">TASKS</h1>
      <div v-for="(getTask, index) in tasks" :key="index" class="text-gray-700 text-sm font-bold">
      <span >
          {{ getTask }}
      </span>
    </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      tasks: [
        'Create a todo app',
        'Listen to music',
        'Drink tea'
      ],
      task: ''
    }
  },

  methods: {
    addTask () {
      this.tasks.push(this.task)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .highlight-title:hover{
    cursor: pointer;
  }
</style>
