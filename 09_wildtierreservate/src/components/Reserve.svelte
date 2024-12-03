<script>
    import Hyena from "./Hyena.svelte";
    import Gnu from "./Gnu.svelte";

    export let w;
    export let h;
    export let plants;
    export let hyenas = 1;
    export let gnus = 2;

    let hyenaArray = new Array(hyenas);
    let gnuArray = new Array(gnus);

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
    {#each gnuArray as _, i}
        <Gnu />
    {/each}

    {#each hyenaArray as _, i}
        <Hyena />
    {/each}
</div>

<style>
    .reserve {
        border: 5px solid brown;
        border-radius: 10px;
    }
</style>
