<script>
    export let animalName = "Nilpferd";
</script>

<div class="card-wrapper">
    <div class="card-content">
        <div class="card-number border-bottom">F2</div>
        <div class="card-title border-bottom">{animalName}</div>
        <img class="card-image" src="images/f2.jpg" alt="{animalName}"/>
        <div class="card-trivia border-bottom">
            Ihre Zähne wachsen ständig nach und werden bis zu 50cm lang.
        </div>
        <div class="stat-box">
            <div class="stat-pair">
                <div class="stat-icon">
                    <img src="images/icons/weight.png" alt="weight" />
                </div>
                <div class="stat-content">4500</div>
            </div>

            <div class="stat-pair">
                <div class="stat-icon">
                    <img src="images/icons/length.png" alt="length" />
                </div>
                <div class="stat-content">500</div>
            </div>

            <div class="stat-pair">
                <div class="stat-icon">
                    <img src="images/icons/age.png" alt="max age" />
                </div>
                <div class="stat-content">50</div>
            </div>

            <div class="stat-pair">
                <div class="stat-icon">
                    <img src="images/icons/speed.png" alt="max speed" />
                </div>
                <div class="stat-content">35</div>
            </div>

            <div class="stat-pair">
                <div class="stat-icon">
                    <img
                        src="images/icons/offspring.png"
                        alt="offspring per cycle"
                    />
                </div>
                <div class="stat-content">1</div>
            </div>

            <div class="stat-pair">
                <div class="stat-icon">
                    <img
                        src="images/icons/death.png"
                        alt="caused yearly human casualties"
                    />
                </div>
                <div class="stat-content">500</div>
            </div>
        </div>
    </div>
</div>

<style>
    .border-bottom {
        border-bottom: var(--thick-line-strength) solid var(--card-dark-color);
    }

    .card-wrapper {
        background-color: var(--card-dark-color);
        padding: 12px;
        display: inline-block;
    }

    .card-content {
        background-color: var(--card-background-color);
        display: grid;
        overflow: hidden;
        width: 200px;
        height: 300px;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(10, 1fr);
        border-radius: 1em;
        font-size: 0.75em;
    }

    .card-number {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #7d982a;
        color: white;
        font-weight: 700;
        font-size: 1.5em;
    }

    .group-a {
        background-color: #c16b10;
    }

    .group-b {
        background-color: #7e362c;
    }

    .group-c {
        background-color: #624c4a;
    }

    .group-d {
        background-color: #633b63;
    }

    .group-e {
        background-color: #445b95;
    }

    .group-f {
        background-color: #7d982a;
    }

    .group-g {
        background-color: #4b634c;
    }

    .group-h {
        background-color: #107a84;
    }

    .card-title {
        grid-column: span 3;
        display: flex;
        align-items: center;
        padding-left: 0.5rem;
        text-transform: uppercase;
        font-weight: 600;
        font-size: 1.25em;
    }

    .card-image {
        grid-column: span 4;
        grid-row: span 5;
        background-color: white;
        width: 100%;
        height: 100%;
        max-width: 100%;
        max-height: 100%;
        object-fit: cover;
    }

    .card-trivia {
        grid-column: span 4;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 0 1em;
        background-color: #949889;
        font-style: italic;
        font-size: 0.85em;
        border-top: 1px solid var(--card-dark-color);
        box-shadow: 2px 0px 10px var(--card-dark-color);
    }

    .stat-box {
        grid-column: span 4;
        grid-row: span 3;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: repeat(3, 1fr);
        gap: var(--thick-line-strength);
        background-color: var(--card-dark-color);
    }

    .stat-pair {
        display: grid;
        grid-template-columns: 1fr 1fr;
        background-color: var(--card-background-color);
    }

    .stat-icon,
    .stat-content {
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 1.2em;
        font-weight: 500;
    }

    .stat-icon {
        background-color: #e0d9cc;
    }

    .stat-icon img {
        max-height: 50%;
        max-width: 50%;
        object-fit: cover;
    }
</style>
