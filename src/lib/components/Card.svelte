<script>
    import { fly } from 'svelte/transition';
    import { backOut } from 'svelte/easing';

    export let post;
    export let i;
</script>

<li in:fly|global={{
    y: 100,
    x: 0,
    delay: 200 * i,
    easing: backOut
}}>
    <article>
        <a href={post.path}>
            <h3>{post.meta.tags}</h3>
            <h2>{post.meta.title}</h2>
            <p>{post.meta.description}</p>
            <img src={post.meta.cover} alt={post.meta.coverDescription}>
        </a>
    </article>
</li>

<style lang="scss">
    $background: #1B4D4C;
    $accentcolor: #B0DDC2;
    article{
        border-top: 2px solid $accentcolor  ;
        box-shadow: 0 2px 4px -1px rgba(0,0,0,0.2),0 4px 5px 0 rgba(0,0,0,0.14),0 1px 10px 0 rgba(0,0,0,0.12);
        padding: 1rem;
        margin-bottom: 1rem;
        background-color: $background;
        min-height: 100%;
    }

    article:hover{
        transform: scale(1.04);
    }
    h2{
        font-size: 2rem;
        font-weight: 700;
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    h2:hover{
        color: $accentcolor;
    }
    h3{
        font-family: 'light';
        color: $accentcolor;
    }
    p{
        margin-bottom: 1rem;
    }
    @media screen and (max-width: 30rem) {
      li{
        margin: auto;
      }
    }
</style>