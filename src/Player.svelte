<script>
  import { createEventDispatcher } from "svelte";
  export let name;
  export let points;
  export let index;

  let showControls = false;

  const dispatch = createEventDispatcher();

  const addPoint = () => (points += 1);
  const removePoint = () => (points -= 1);
  const toggleControl = () => (showControls = !showControls);

  const removePlayer = () => {
    dispatch("removeplayer", index);
  };
</script>

<div class="card">
  <h1>
    {name}
    <button class="btn btn-sm" on:click={toggleControl}
      >{#if showControls}
        -
      {:else}+{/if}</button
    >
    <button class="btn btn-sm btn-danger" on:click={removePlayer}>x</button>
  </h1>
  <h3>Points: {points}</h3>
  {#if showControls}
    <button class="btn" on:click={addPoint}>+1</button>
    <button class="btn btn-dark" on:click={removePoint}>-1</button>
    <input type="number" bind:value={points} />
  {/if}
</div>

<style>
  h1 {
    color: #204f6e;
  }
  h3 {
    margin-bottom: 10px;
  }
</style>
