<script>
    import imgMusculacao from '$lib/assets/musculacao.jpg'
    import iconMuscle from '$lib/assets/icon-muscle.png'

    export let title = "Você esta pronto <br /> para o desafio?"
    export let content = 'A Academia Local está pronta para te ajudar a chegar mais longe e alcançar sua melhor performance.'
    export let btn = "Saiba mais"
    export  let href

    export let img
    if (img === 'musculacao') img = imgMusculacao

    export let icon
    if (icon === 'muscle') icon = iconMuscle

</script>

<section class="intro" style="background-image: url({img});">
    <div class="intro__wrapper wrap">
        <h1>{@html title} <img src="{icon}" alt=""></h1>
        <p>{content}</p>

        {#if btn && href}
        <a class="btn" href="{href}">{btn}</a>
        {/if}
        
    </div>
</section>

<style>
    .intro{
        min-height: 360px;
        background-size: cover;
        background-position: center;
        display: grid;
        align-content: center;
        justify-content: start;
        position: relative;
    }
    .intro::after{
        content: '';
        position: absolute;
        inset: 0;
        background-color: rgba(0, 0, 0, 0.55);
    }
    .intro__wrapper{
        z-index: 1;
        max-width: 450px;
    }
    .btn{
        margin-top: 24px;
    }
    p{
        font-size: calc(18/16*1rem);
        margin-top: 16px;
    }
    img{
        display: inline;
        max-width: 36px;
    }
</style>