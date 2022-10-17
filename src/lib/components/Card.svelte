<script>
    export let post;
</script>

<article>
    <a href={post.path}>
        <h3>{post.meta.tags}</h3>
        <h2>{post.meta.title}</h2>
        <p>{post.meta.description}</p>
        <img src={post.meta.cover} alt={post.meta.cover_description}>
    </a>
</article>