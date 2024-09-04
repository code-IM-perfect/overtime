<script>
    import { onMount } from 'svelte';
    import { writable } from 'svelte/store';

    let tasks = writable([]);

    // Fetch tasks from the API
    onMount(async () => {
        const res = await fetch('/api/getTasks');
        tasks.set(await res.json());
    });

    // Function to handle task deletion or other actions
    // function handleTaskAction(taskId, action) {
    //     // Call API to perform the action
    //     fetch(`/api/task/${taskId}`, {
    //         method: 'POST',
    //         headers: {
    //             'Content-Type': 'application/json'
    //         },
    //         body: JSON.stringify({ action })
    //     })
    //     .then(response => response.json())
    //     .then(data => {
    //         // Update tasks list
    //         tasks.update(t => t.filter(task => task.id !== taskId));
    //     });
    // }
</script>

<main>
    <div class="dashboard-head">
        <h1>Task Management Dashboard</h1> 
        
    </div>
    {#if $tasks.length === 0}
        <p>No tasks available. Add some tasks to get started.</p>
    {:else}
        <ul>
            {#each $tasks as task}
                <li>
                    <h2>{task.name}</h2>
                    <p>Required Time: {task.time} hours</p>
                    <p>Expertise Level: {task.expertise}</p>
                    <p>Hourly Wage: ${task.wage}</p>
                    <p>Deadline: {new Date(task.deadline).toLocaleString()}</p>
                    <p>Divisible: {task.divisible ? 'Yes' : 'No'}</p>
                    <!-- <button class="important" on:click={() => handleTaskAction(task.id, 'delete')}>Delete Task</button> -->
                </li>
            {/each}
        </ul>
    {/if}
</main>

<style>
    .dashboard-head{
        display: flex;
        margin-bottom: 1rem;
        align-items: center;
    }

    h1{
        flex: 1;
        font-weight: 600;
        font-size: 2rem;
    }

    ul {
        list-style: none;
        padding: 0;
    }

    li {
        border-bottom: 1px solid #ddd;
        padding: 15px 0;
    }

    h2 {
        margin: 0 0 10px;
    }

    button.important {
        padding: 5px 10px;
        background-color: #dc3545;
        color: white;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }

    button.important:hover {
        background-color: #c82333;
    }
</style>
