<script>
  import Reserve from "./components/Reserve.svelte";
  import { getRandomInt } from "./assets/utils";

  let reserveCount = getRandomInt(3, 5);
  let reserveArray = new Array(reserveCount);
</script>

<header>
  <h1>Wildtierreservate</h1>
</header>
<main>
  <div id="reserve-wrapper">
    {#each reserveArray as reserve, i}
      <Reserve
        w={getRandomInt(50, 300)}
        h={getRandomInt(50, 300)}
        plants={getRandomInt(0, 100)}
        hyenas={getRandomInt(2, 6)}
        gnus={getRandomInt(6, 20)}
      />
    {/each}
  </div>
</main>

<style>
  #reserve-wrapper {
    display: flex;
    max-width: 1200px;
    margin: auto;
    justify-content: center;
    gap: 1em;
  }
</style>
