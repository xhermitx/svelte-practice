<script>
    import {v4 as uuid} from 'uuid';

    import Button from "./Button.svelte";
    export let todos = [];
    export let title = '';
    export let completed = false;

    function handleTodo() {

        // todos.push({
        //     id: uuid(),
        //     title: title,
        //     completed: completed,
        // })
        // todos = todos

        todos = [...todos, {
            id: uuid(),
            title: title,
            completed: completed,
        }]

        console.log(todos)
    }

</script>

<div class="todo-list-wrapper">
<ul>
{#each todos as {id, title}, index (id)}
    <!-- {@const number = index + 1} -->
    <li>{index + 1} - {title}</li>
{/each}
</ul>

<form on:submit|preventDefault={handleTodo}>
    <input placeholder="title" bind:value={title}/>
    <br>
    <label for="status">Status</label>
    <input type="checkbox" name="status" bind:value={completed}/>
    <br>

    <Button type="submit">Add</Button>
</form>

</div>