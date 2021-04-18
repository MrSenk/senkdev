<script>
  import { fade, fly } from "svelte/transition";
  import Navbar from "./components/navbar/Navbar.svelte";
  import MainText from "./components/maintext/MainText.svelte";
  import Experience from "./components/experience/Experience.svelte";
  let selectedPage = 0;

  const switchContent = (event) => {
    selectedPage = event.detail;
  };
</script>

<div class="container">
  <Navbar on:switchcontent={switchContent} />
  {#if selectedPage === 0}
    <div in:fly={{ x: 200, duration: 500 }}>
      <MainText />
    </div>
  {:else if selectedPage === 1}
    <div in:fly={{ x: 200, duration: 500 }}>
      <Experience />
    </div>
  {:else if selectedPage === 2}
    <div in:fly={{ x: 200, duration: 500 }}>
      <MainText />
    </div>
  {/if}
</div>
