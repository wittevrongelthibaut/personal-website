<script>
    import { fly } from 'svelte/transition';
    import { backOut } from 'svelte/easing';

    export let post;
    export let i;

    const topColor = post.meta.topColor[0]
</script>

<li in:fly={{
    y: 100,
    x: 0,
    delay: 200 * i,
    easing: backOut
}}>
    <article style="--top-color: {topColor}">
        <a href={post.path}>
            <h3>{post.meta.tags}</h3>
            <h2>{post.meta.title}</h2>
            <p>{post.meta.description}</p>
            <img src={post.meta.cover} alt={post.meta.coverDescription}>
        </a>
    </article>
</li>

<style>
    article{
        border-top: 2px solid var(--top-color);
        box-shadow: 0 2px 4px -1px rgba(0,0,0,0.2),0 4px 5px 0 rgba(0,0,0,0.14),0 1px 10px 0 rgba(0,0,0,0.12);
        padding: 1rem;
        margin-bottom: 1rem;
        background-color: #1c1b1b;
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
        color: var(--top-color);
    }
    h3{
        font-family: 'light';
        color: var(--top-color);
    }
    p{
        margin-bottom: 1rem;
    }
</style>