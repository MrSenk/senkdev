<script>
  import { createEventDispatcher } from "svelte";
  const dispatch = createEventDispatcher();

  const switchContent = (page) => {
    dispatch("switchcontent", page);
  };
</script>

<div class="navbar d-flex justify-content-between">
  <div class="navbar-name col-7">Camilo Cuevas</div>
  <div class="d-flex col-5 justify-content-around">
    <div class="navbar-link" on:click={() => switchContent(0)}>
      <span>Home</span>
      <div class="navbar-underline mt-1" />
    </div>
    <div class="navbar-link" on:click={() => switchContent(1)}>
      <span>Experience</span>
      <div class="navbar-underline mt-1" />
    </div>
    <div class="navbar-link" on:click={() => switchContent(2)}>
      <span>Contact</span>
      <div class="navbar-underline mt-1" />
    </div>
  </div>
</div>

<style>
  .navbar-name {
    color: white;
    font-size: 3em;
    font-weight: 500;
  }
  .navbar-link {
    color: white;
    font-size: 1.7em;
    cursor: pointer;
    font-weight: 500;
    transition: 0.15s;
  }
  .navbar-link:hover {
    color: #61b6f4;
  }
  .navbar-underline {
    border: 2px #61b6f4 solid;
    border-radius: 5px;
  }
</style>
