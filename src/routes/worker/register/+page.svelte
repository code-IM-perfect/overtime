<script>
    import { writable } from 'svelte/store';
    let availibility = writable(1);
    let expertise = writable(1);
    let min_hourly_wage = writable(25);
    let accepted = writable(false);

    function register(){

    }
</script>
<div class="w-full h-[80vh] flex justify-center items-center">
    <main class="form-card">
        <h1>Register</h1>
        <br>
        <form on:submit|preventDefault={register}>
            <div>
                <label for="adress">Wallet address:</label>
                <input type="text" id="address" required value={"0x1111111254fb6c44bAC0beD2854e76F90643097d"} />
            </div>
            <div>
                <label for="expertise">Expertise Level:</label>
                <input type="number" id="expertise" bind:value={$expertise} min="1" required />
            </div>
    
            <div>
                <label for="availibility">Availibility (in hours) : </label>
                <input id="availibility" type="number" bind:value={$availibility} min={1} step={1} required  />
            </div>
            <div>
                <label for="wage">Hourly Wage (in $) :</label>
                <input id="wage" type="number" bind:value={$min_hourly_wage} min={1} step={1} required />
            </div>
            <div class="checkbox">
                <label for="accept">Accept Terms and Conditions:</label>
                <input id="accept" type="checkbox" required bind:checked={$accepted} />
            </div>
            <button class="action"><a href="/worker">Register</a></button>
        </form>
    </main>
</div>