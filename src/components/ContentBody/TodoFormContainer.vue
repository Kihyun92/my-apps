<template>
    <div class="todo-form-container">
        <input class="input-box"
            type="text"
            v-model="todo"
            placeholder="할일을 입력하세요.">
        <button class="add-btn" @click.prevent="addTodos">등록</button>
    </div>
</template>

<script>
export default {
    name: 'TodoFormContainer',
    data() {
        return {
            todo: ''
        }
    },
    methods: {
        addTodos() {
            this.$emit('addTodos', this.todo);
            return this.todo = '';
        }
    }
}
</script>

<style>
.todo-form-container {
    border-bottom: 1px solid grey;
}
.input-box {
    border: 1px solid black;
}
.add-btn{
    border: 1px solid;
}
</style>