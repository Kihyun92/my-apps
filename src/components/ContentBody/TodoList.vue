<template>
    <div class="todo-container">
        <todo-form-container v-on:addTodos="setTodos"></todo-form-container>
        <ul>
            <li class="todo-item"
                v-for="(todo, index) in todos"
                :key="index">
                <todo-item :todo="todo"></todo-item>
            </li>
        </ul>
    </div>
</template>


<script>
import TodoFormContainer from './TodoFormContainer';
import TodoItem from './TodoItem';

export default {
    name: 'TodoList',
    data() {
        return {
            todos: [],
            isModify: false
        };
    },
    components: {
        TodoFormContainer,
        TodoItem
    },
    methods: {
        setTodos(todo) {
            this.todos.push(todo);
        }
    }
}
</script>


<style>
    .todo-container {
        border: 1px solid black;
        width: 90%;
        /* display: table; */
        margin-left: auto;
        margin-right: auto;
    }
    .todo-item {
        border-bottom: 1px solid black;
    }
</style>

