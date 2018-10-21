<template>
    <div class="todo-container">
        <ul>
            <li class="todo"
                v-for="(todo, index) in todos"
                :key="index">
                {{todo}}
            </li>
        </ul>
    </div>
</template>


<script>
export default {
    name: 'TodoList',
    data() {
        return {
            todos: ['책보기', '앱 만들기', '테스트코드 작성', '', '', '', '']
        };
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
    .todo {
        border-bottom: 1px solid black;
    }
</style>

