<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todos">
            <TodoI v-bind:todo="todo" v-on:del-todo="$emit('del-todo',todo.id)"/>
        </div>
    </div>
</template>
<script>
import TodoI from './TodoItem.vue';

export default {
    name:"Todos",
    components: {
        TodoI
    },
    props: ["todos"]
}
</script>
<style scoped>

</style>