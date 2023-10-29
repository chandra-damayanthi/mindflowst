<style>
    h1 {
        font-family: Arial, Helvetica, sans-serif;
        letter-spacing: -1px;
        color: rgb(134, 109, 191);
    }
</style>

<script lang="ts">
    export let items:string[] = [];
    let workThought = '';
     function addWorkThought() {
        if (workThought.trim() !== '') {
            items = [...items, workThought];
            workThought = '';
        }
    }

</script>

<h1>Mindflowst</h1>
<ul>
    {#each items as item (item)}
        <li>{item}</li>
    {/each}
</ul>
<label>
    Workthought 
    <input type="text" bind:value={workThought}>
</label>



<button on:click={addWorkThought}>Add</button>