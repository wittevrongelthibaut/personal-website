    <script>
	      import Card from './../../lib/components/Card.svelte';
	      import { dateFormater } from '$lib/utils/index.js';
        export let data
    </script>
    
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