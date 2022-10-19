<script>
	  import { name } from '$lib/config/config.js';
    import Card from '$lib/components/Card.svelte';
    export let data
</script>

<svelte:head>
  <title>Welcome to {name}'s blog</title>
  <meta name="description" content="Welcome to my blog where all my blogposts can be found!">
  <meta property="og:title" content="Welcome to {name}'s blog" />
  <meta property="og:description" content="Welcome to {name}'s blog" />
	<meta property="og:url" content="https://thibautwittevrongel.com/blog" />
</svelte:head>

<h1>Blog</h1>
  
<ul>
  {#each data.posts as post, i}
      <Card post={post} i={i}/>
  {/each}
</ul>

<style>
  h1{
    font-family: headings;
    font-size: 2rem;
    margin-bottom: 2rem;
  }

  ul{
      display: grid;
      grid-template-columns: repeat(auto-fill,minmax(25rem,1fr));
      gap: 2rem;
      padding: 0;
   }
  </style>