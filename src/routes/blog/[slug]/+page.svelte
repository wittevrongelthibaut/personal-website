<script>
	import { dateFormater } from '$lib/utils/index.js';
  import '$lib/styles/blogpost.scss';
  export let data;
</script>

<svelte:head>
  <title>{data.title} - Thibaut Wittevrongel blog</title>
  <meta name="description" content={data.description}>

  <meta property="og:title" content={data.title} />
  <meta property="og:description" content={data.description}/>
  <meta property="og:url" content={`https://thibautwittevrongel.com${data.currentRoute}`}/>
</svelte:head>
  
<article>
  <h3>{data.tags}</h3>
  <h1>{ data.title }</h1>
  <section id='publishData'>
    <h2> Published by: {data.author} on {dateFormater(data.date)}</h2>
  </section>
  <section id='content'>
    <svelte:component this={data.content} />
  </section>
</article>

<style lang='scss'>
  $accentColor: #B0DDC2;
  $bordercolor: #7EB694;
  article{
    width: 75%;
    margin-left: auto;
    margin-right: auto;
    border-top: 2px solid $accentColor;
    padding: 1rem;
    margin-top: 5rem;
  }
  h1{
    font-size: 3rem;
  }
  h3{
    font-family: 'light';
    color: $accentColor;
    margin-top: 1rem;
    margin-bottom: 1rem;
  }

  #publishData{
    color: $bordercolor;
    font-size: 1rem;
    margin-top: 0.5rem;
    margin-bottom: 2rem;
  }

  @media only screen and (max-width: 60rem) {
  article{
      width: 100%;
  }
}

</style>