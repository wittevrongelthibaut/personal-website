<script>
	import { dateFormater } from '$lib/utils/index.js';
  import '$lib/styles/blogpost.scss';
  export let data;

  const topColor = data.topColor
</script>

<svelte:head>
  <title>{data.title} - Thibaut Wittevrongel blog</title>
  <meta property="og:title" content={data.title} />
</svelte:head>
  
<article style="--top-color: {topColor}">
  <h3>{data.tags}</h3>
  <h1>{ data.title }</h1>
  <section id='publishData'>
    <h2> Published by: {data.author} on {dateFormater(data.date)}</h2>
  </section>
  <section id='content'>
    <svelte:component this={data.content} />
  </section>
</article>

<style>
  article{
    width: 75%;
    margin-left: auto;
    margin-right: auto;
    border-top: 2px solid var(--top-color);
    padding: 1rem;
  }
  h1{
    font-size: 3rem;
  }
  h3{
    font-family: 'light';
    color: var(--top-color);
    margin-top: 1rem;
    margin-bottom: 1rem;
  }

  #publishData{
    color: gray;
    font-size: 1rem;
    margin-top: 0.5rem;
    margin-bottom: 2rem;
  }

</style>