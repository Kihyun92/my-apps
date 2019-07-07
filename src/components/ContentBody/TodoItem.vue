<template>
    <div>
        <input v-if="isModify" type="text" :placeholder="inputTodo" v-model="inputTodo">
        <div v-else @click="modifyTodo">{{todo}}</div>
    </div>
</template>

<script>
export default {
    name: 'TodoItem',
    props: {
        todo: {
            type: String,
            default: ''
        }
    },
    data() {
        return {
            isModify: false
        }
    },
    computed: {
        inputTodo() {
            return this.todo;
        }
    },
    methods: {
        modifyTodo() {
            this.isModify = true;
        }
    }
}
</script>