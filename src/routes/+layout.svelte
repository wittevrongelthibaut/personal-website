<script>
  import Header from '$lib/components/Header.svelte'
  import '$lib/styles/style.scss'
  import { fade } from 'svelte/transition'
	import SocialLinks from '../lib/components/SocialLinks.svelte';
  
  export let data
</script>

<Header />

{#key data.currentRoute}
  <main in:fade|global={{ duration: 150, delay: 200 }} out:fade|global={{ duration: 200 }}>
    <slot />
  </main>
{/key}

<SocialLinks />