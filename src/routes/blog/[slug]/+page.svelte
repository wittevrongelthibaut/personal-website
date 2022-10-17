<script>
	import { dateFormater } from '$lib/utils/index.js';
    export let data;
</script>

<svelte:head>
  <title>{data.title} - Thibaut Wittevrongel blog</title>
  <meta property="og:title" content={data.title} />
</svelte:head>
  
<article>
  <h1>{ data.title }</h1>
  <p>Published: {dateFormater(data.date)}</p>
  <svelte:component this={data.content} />
</article>