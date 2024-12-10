<script>
  let selectedType = "";
  let bodies = [];

  async function fetchBodies() {
    const response = await fetch(
      `https://api.le-systeme-solaire.net/rest/bodies?filter[]=bodyType,eq,${selectedType}`,
    );
    const data = await response.json();
    bodies = data.bodies;
    console.log(bodies);
  }

  function handleSelectionChange(event) {
    selectedType = event.target.value;
    fetchBodies();
  }
</script>

<select on:change={handleSelectionChange}>
  <option value="Planet">Planets</option>
  <option value="Moon">Moons</option>
  <option value="Dwarf Planet">Dwarf Planets</option>
</select>

{#if bodies.length > 0}
  <p>{bodies.length} bodies found.</p>
{/if}

<ul>
  {#each bodies as body}
    <li>{body.englishName}</li>
  {/each}
</ul>
