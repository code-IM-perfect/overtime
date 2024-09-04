<script>
    import { onMount } from 'svelte';
    import { writable } from 'svelte/store';

    // Stores for form inputs
    let time = writable(1);
    let expertise = writable(1);
    let dependencies = writable([]);
    let wage = writable(25);
    let deadline = writable('');
    let divisible = writable(false);

    // Sample tasks for dependencies
    let allTasks = [
        { id: 1, name: "Task 1" },
        { id: 2, name: "Task 2" },
        { id: 3, name: "Task 3" }
    ];

    // Function to handle form submission
    function addTask() {
        const task = {
            time: $time,
            expertise: $expertise,
            dependencies: $dependencies.map(dep => parseInt(dep)),
            wage: $wage,
            deadline: new Date($deadline).getTime(),
            divisible: $divisible
        };

        // Simulate sending data to server
        console.log("Task added:", task);

        // Reset form fields after submission
        $time = 1;
        $expertise = 1;
        $dependencies = [];
        $wage = 25;
        $deadline = '';
        $divisible = false;
    }
</script>

<main class="form-card bg-dark">
    <h1>Add a Task</h1>
    <br>
    <form on:submit|preventDefault={addTask}>
        <div>
            <label for="time">Required Time (hours):</label>
            <input type="number" id="time" bind:value={$time} min="1" required />
        </div>
        <div>
            <label for="expertise">Expertise Level:</label>
            <input type="number" id="expertise" bind:value={$expertise} min={1} required />
        </div>
        <div>
            <label for="dependencies">Dependencies:</label>
            <select id="dependencies" bind:value={$dependencies} multiple>
                {#each allTasks as task}
                    <option value={task.id}>{task.name}</option>
                {/each}
            </select>
        </div>
        <div>
            <label for="wage">Hourly Wage:</label>
            <input id="wage" type="number" bind:value={$wage} min="1" required />
        </div>
        <div>
            <label for="deadline">Deadline:</label>
            <input id="deadline" type="datetime-local" bind:value={$deadline} required />
        </div>
        <div class="checkbox">
            <label for="divisible">Divisible:</label>
            <input id="divisible" type="checkbox" bind:checked={$divisible} />
        </div>
        <button on:submit={addTask} class="action">Add Task</button>
    </form>
</main>
