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
        /* border : 2px solid #73AD21; */
    }
</style>
