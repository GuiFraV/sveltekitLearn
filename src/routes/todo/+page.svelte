<script lang="ts">
    let todos: string[] = [];
    let newTodo: string = '';

    function addTodo() {
        if (newTodo.trim() !== '') {
            todos = [...todos, newTodo];
            newTodo = '';
        }
    }

    function removeTodo(index: number) {
        todos = todos.filter((_, i) => i !== index);
    }
</script>

<main>
    <h1>Todo List</h1>

    <input type="text" bind:value={newTodo} placeholder="Enter a new todo" />
    <button on:click={addTodo}>Add Todo</button>

    <ul>
        {#each todos as todo, index}
            <li>
                {todo}
                <button on:click={() => removeTodo(index)}>Remove</button>
            </li>
        {/each}
    </ul>
</main>

<style>
    main {
        max-width: 400px;
        margin: 0 auto;
        padding: 20px;
    }

    input, button {
        margin-bottom: 10px;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 5px;
    }
</style>
