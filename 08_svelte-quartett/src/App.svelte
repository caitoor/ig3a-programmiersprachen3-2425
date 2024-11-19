<script>
    import Card from "./components/Card.svelte";
</script>

<div id="wrapper">
    <header>
        <h1>Tierquartett</h1>
        <nav>
            <ul>
                <li><a href="#" class="active">Übersicht</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <Card animalName="Krokodil"/>
        <Card animalName="Elefant"/>
        <Card animalName="Giraffe"/>
        <Card animalName="Nashorn"/>
        <Card />
    </main>
    <footer>
        <p>Made with ❤️ by IG3 – Programmiersprachen 3</p>
    </footer>
</div>

<style>
</style>
