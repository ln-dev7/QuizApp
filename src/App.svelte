<script>
    import Card from './components/Choice.svelte'
    import {cards} from './dataBase/cards'
</script>

<h1><span>Q</span>uiz <span>A</span>pp <h2>Faites un choix et testez vos connaissances</h2></h1>
<div class="container-cards">
    {#each cards as card}
        <Card title={card.nom} url={card.url} />
    {/each}
</div>

<style>
    h1{
        text-align: center;
        color: #fff;
    }
    h2{
        color: #adadad;
        font-size: 0.5em;
    }
    span{
        color: red;
    }
    .container-cards{
        /* height: 100vh; */
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
    }
</style>