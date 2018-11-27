<template>
    <div class="body-container">
        Todo list section!
        <todo-list></todo-list>
    </div>
</template>


<script>
import todoList from './TodoList';

export default {
    name: 'ContentBody',
    components: {
        todoList
    }
}
</script>


<style>
    .body-container {
        padding-top: 10px;
    }
</style>
