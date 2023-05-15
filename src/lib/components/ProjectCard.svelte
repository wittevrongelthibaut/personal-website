<script>
    export let post;
</script>

<li>
    <article>
        <a href={post.path} target="_blank">
            <h2>{post.title}</h2>
            <p>{post.description}</p>
            <img src={post.cover} alt={post.coverDescription}>
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
    p{
        margin-bottom: 1rem;
    }
    @media screen and (max-width: 30rem) {
      li{
        margin: auto;
      }
    }
</style>