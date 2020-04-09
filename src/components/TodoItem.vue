<template>
    <li>
        <span v-bind:class="{done: todo.completed}">
            <input type="checkbox" @change="todo.completed = !todo.completed">
            <strong>{{index + 1}}</strong>
            {{todo.title | uppercase}}

        </span>
        <button class="rm" @click="$emit('removeTodo', todo.id)">&times;</button>
    </li>
</template>

<script>
export default {
    name: 'TodoItem',
    props: {
        todo: {
            type: Object,
            required: true
        },
        index: Number
    },
    filters: {
        uppercase(value) {
            return value.toUpperCase()
        }
    }
}
</script>

<style scoped>
    li {
        border: 1px solid #2c3e50;
        display: flex;
        justify-content: center;
        padding: .5rem 2rem;
        margin-bottom: 2rem;
    }

    .rm {
        display: inline-block;
        background: red;
        color: #fff;
        border-radius: 50%;
        font-weight: bold;
        border: none;
        padding: 5px;
        margin-left: 30px;
    }

    input {
        margin-right: 1rem;
    }

    .done {
        text-decoration: line-through;
    }


</style>