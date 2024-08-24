<script>

  import Todolist from "./lib/TodoList.svelte";
  import { v4 as uuid} from "uuid";

  let todos = [
    {
      id: uuid(),
      title: 'Todo 1',
      completed: true
    },
    {
      id: uuid(),
      title: 'Todo 2',
      completed: false
    }
  ];

</script>


<h2>{todos.length} Todos</h2>
<Todolist bind:todos />

<style>

</style>