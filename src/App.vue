<template>
<div id="app">
    <h1>Todo Application</h1>
    <hr>

    <router-view />
</div>
</template>

// <script>
// import TodoList from '@/components/TodoList'
// import AddTodo from '@/components/AddTodo'

// export default {
//     name: 'app',
//     components: {
//         TodoList,
//         AddTodo
//     },
//     data() {
//         return {
//             todos: [
//                 // {
//                 //     id: 1,
//                 //     title: 'Something 1',
//                 //     completed: false
//                 // },
//                 // {
//                 //     id: 2,
//                 //     title: 'Something 2',
//                 //     completed: false
//                 // },
//                 // {
//                 //     id: 3,
//                 //     title: 'Something 3',
//                 //     completed: false
//                 // },
//                 // {
//                 //     id: 4,
//                 //     title: 'Something 4',
//                 //     completed: false
//                 // }
//             ]
//         }
//     },
//     mounted() {
//         fetch('https://jsonplaceholder.typicode.com/todos?_limit=3')
//             .then(response => response.json())
//             .then(json => this.todos = json)
//     },
//     methods: {
//         removeTodo(id) {
//             this.todos = this.todos.filter(t => t.id !== id)
//         },
//         addTodo(todo) {
//             this.todos.push(todo)
//         }
//     }
// }
// </script>

<style lang="scss">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}

#nav {
    padding: 30px;

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
            color: #42b983;
        }
    }
}
</style>
