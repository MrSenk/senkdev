<script>
  import Navbar from "./Navbar.svelte";
  import Player from "./Player.svelte";
  import AddPlayer from "./AddPlayer.svelte";

  let players = [
    {
      name: "Camilo Cuevas",
      points: 54,
    },
    {
      name: "Matias Molina",
      points: 45,
    },
    {
      name: "Piter Piter",
      points: 35,
    },
  ];

  const addPlayer = (e) => {
    const newPlayer = e.detail;
    players = [...players, newPlayer];
  };

  const removePlayer = (e) => {
    const index = e.detail;
    players = [...players.slice(0, index), ...players.slice(index + 1)];
  };
</script>

<Navbar />
<div class="container">
  <AddPlayer on:addplayer={addPlayer} />
  {#if players.length === 0}
    <p>No Players</p>
  {:else}
    {#each players as player, i}
      <Player
        name={player.name}
        points={player.points}
        index={i}
        on:removeplayer={removePlayer}
      />
    {/each}
  {/if}
</div>
