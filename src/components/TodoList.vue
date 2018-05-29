<template>
    <div class="main">
        <ul class="todo-list">
          <li class="todo" v-for="todo in filteredTodos" :class="{completed: todo.completed}">
            <div class="view"><!-- v-bin:class = :class -->
              <input type="checkbox" class="toggle" v-model="todo.completed">
              <label for="">{{ todo.name }}</label>
              <button class="destroy" @click.prevent="deleteTodo(todo)"></button>
            </div>
          </li>
        </ul>
      </div>
</template>

<script>
export default {
    name: 'TodoList',
    props: {
        filteredTodos: Array
    }
};
</script>

<style>
</style>
