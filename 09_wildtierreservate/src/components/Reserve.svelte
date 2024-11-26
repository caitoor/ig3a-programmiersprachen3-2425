<script>
    import Hyena from "./Hyena.svelte";

    export let w;
    export let h;
    export let plants;
    export let hyenas = 1;

    /*  function generateHyenasArray(hyenas) {
        return Array.from({ length: hyenas }, (_, index) => `Hyena ${index + 1}`);
    } 

    const hyenasArray = generateHyenasArray(hyenas);

    */

    function mapColor(value, start = [243, 245, 159], end = [54, 99, 12]) {
        value = value / 100;
        const r = start[0] + (end[0] - start[0]) * value;
        const g = start[1] + (end[1] - start[1]) * value;
        const b = start[2] + (end[2] - start[2]) * value;
        return `rgb(${r}, ${g}, ${b})`;

        /* rgb(134, 211, 14) */
    }

    const reserveColor = mapColor(plants);
</script>

<div
    class="reserve"
    style="width: {w}px; height: {h}px; background-color:{reserveColor};"
>
    {#each { length: hyenas } as _, i}
        <Hyena />
    {/each}
</div>

<style>
    .reserve {
        border: 5px solid brown;
        border-radius: 10px;
    }
</style>
