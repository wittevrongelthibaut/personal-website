    <script>
	import Card from './../../lib/components/Card.svelte';
	import { dateFormater } from '$lib/utils/index.js';
        export let data
    </script>
    
    <h1>Blog</h1>
      
    <ul>
      {#each data.posts as post}
        <li>
          <Card post={post}/>
        </li>
      {/each}
    </ul>