<script>
    import AvailableTask from '../../components/+AvailableTask.svelte';
    import RunningTask from '../../components/+RunningTask.svelte';
    import UserProfile from '../../components/+userProfile.svelte';
    
    let count = 0;
    let currentComponent = AvailableTask; // Default component
  
    // function changeTable() {
    //   if (count === 0) {
    //     currentComponent = AvailableTask;
    //     count = 1;
    //   } else {
    //     currentComponent = RunningTask;
    //     count = 0;
    //   }
    //   console.log(currentComponent);
    // }
    let activity1 = "active";
    let activity2 = "inactive";
    function available()
    {
      currentComponent = AvailableTask;
      activity1 = "active";
      activity2 = "inactive";
    }
    function allocated()
    {
      currentComponent = RunningTask;
      activity1 = "inactive";
      activity2 = "active";
    }
      
  </script>
  
  <main>
    <UserProfile />
    <br>

    <!-- <button on:click={changeTable}>Change Table</button> -->
     <div class = "tab-container">
    <div class="button-container">
      <button class={activity1} on:click={available}>Available Tasks</button>
      <button class={activity2} on:click={allocated}>Allocated Tasks</button>
  </div>
</div>
    <!-- Dynamically render the current component -->
    <svelte:component this={currentComponent} />
    
    <br>
    <style>
      .button-container {
          display: flex;
          gap: 10px; 
          margin: 2%;
      }
      .initial {
          padding: 10px 20px; 
          border: 2px solid #333; 
          border-radius: 5px;
          background-color: #50fcb4;
          cursor: pointer;
          font-size: 16px;
          transition: background-color 0.3s ease; 
      }
      .active {
          padding: 10px 20px; 
          border: 2px solid #333; 
          border-radius: 5px;
          background-color: #50fcb4;
          cursor: pointer;
          font-size: 16px;
          transition: background-color 0.3s ease; 
      }
      .inactive {
          padding: 10px 20px; 
          border: 2px solid #333; 
          border-radius: 5px;
          background-color: white;
          cursor: pointer;
          font-size: 16px;
          color : black;
          transition: background-color 0.3s ease; 
      }

      .active:hover {
          /* background-color: #ddd;  */
          opacity: 0.8;
      }
      .inactive:hover {
          background-color: #b4fadd; 

      }
  </style>
  </main>
  