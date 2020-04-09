<template>
    <div>
        <ul>
            <TodoItem
                v-for="(todo, i) in todos"
                v-bind:todo="todo"
                v-bind:index="i"
                :key="todo.id"
                @removeTodo="removeTodo"
             />
        </ul>
    </div>
</template>

<script>
import TodoItem from '@/components/TodoItem'


export default {
    name: 'TodoList',
    components: {
        TodoItem
    },
    props: ['todos'],
    methods: {
        removeTodo(id) {
            this.$emit('removeTodo', id)
        }
    }
}
</script>

<style scoped>
    ul {
        list-style: none;
        margin: 0;
        padding: 0;
    }
</style>