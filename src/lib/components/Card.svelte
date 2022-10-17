<script>
    export let post;

    const topColor = post.meta.topColor[0]
</script>

<article style="--top-color: {topColor}">
    <a href={post.path}>
        <h3>{post.meta.tags}</h3>
        <h2>{post.meta.title}</h2>
        <p>{post.meta.description}</p>
        <img src={post.meta.cover} alt={post.meta.coverDescription}>
    </a>
</article>

<style>
    article{
        border-top: 2px solid var(--top-color);
        box-shadow: 0 2px 4px -1px rgba(0,0,0,0.2),0 4px 5px 0 rgba(0,0,0,0.14),0 1px 10px 0 rgba(0,0,0,0.12);
        padding: 1rem;
        margin-bottom: 1rem;
    }
    h2{
        font-size: 2rem;
        font-weight: 700;
    }
    h3{
        font-family: 'light';
        color: var(--top-color);
    }
</style>