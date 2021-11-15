<script>
    export let title;
    export let url;
</script>

<div class="card">
    <h2>{title}</h2>
    <div class="card-image">
        <img src={url} alt="">
    </div>
    <button class="card-button">Commencer le Quiz </button>
</div>

<style>
    .card{
        background: #fff;
        width: 300px;
        margin: 1.5rem;
        box-shadow: 0px 5px 8px #00000080;
        border-radius: 4px;
        display: flex;
        overflow: hidden;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    h2{
        margin: 0.5rem;
        transition: transform .3s ease-in-out;
    }
    .card:hover h2{
        transform: translateY(160px);
        z-index: 2;
    }
    .card-image img{
        object-fit: cover;
        /* transition: transform .3s ease; */
    }
    .card-image{
        transition: transform .3s ease;
    }
    .card:hover .card-image{
        opacity: 0.5;
        transform: scale(2);
    }
    .card-button{
        position: relative;
        border-radius: 2px;
        margin: 0.5rem;
        padding-left: 1.5rem;
        padding-right: 1.5rem;
        background: red;
        color: white;
        cursor: pointer; 
        transition: opacity .3s ease;
    }
    .card-button:hover{
        opacity: 0.6;
    }
    .card-button::before{
        content: '';
        position: absolute;
        top: 50%;
        left: 15px;
        background: #fff;
        width: 3px;
        height: 3px;
        border-radius: 50%;
    }
</style>