<script>
  let todos = [
    {todoName: 'Ireport si Monis', isCompleted: false},
    {todoName: 'Program 2 hrs a day', isCompleted: false},
    {todoName: 'Magsaing', isCompleted: true},
    {todoName: 'Mag grocery', isCompleted: false}
  ];

  const addTodo = (userInput) => {
    const tempArray = [{todoName: userInput, isCompleted: false}];
    todos = todos.concat(tempArray);
  };

  let userInput;
</script>

<style>
  .complete {
    text-decoration: line-through;
  }
</style>

<div>
  <ol>
    {#each todos as task}
      <li class:complete={task.isCompleted}>{task.todoName}</li>
    {/each}
  </ol><br><br><br>
  <h1>{userInput}</h1>
  <input type="text" bind:value={userInput}/>
  <button class="btn btn-primary" on:click={addTodo}>
    Add Task
  </button>
</div>
