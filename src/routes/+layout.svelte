<script>
  import Header from '$lib/components/Header.svelte'
  import '$lib/styles/style.scss'
  import { fade } from 'svelte/transition'
  
  export let data
</script>

<Header />

{#key data.currentRoute}
  <main in:fade={{ duration: 150, delay: 200 }} out:fade={{ duration: 200 }}>
    <slot />
  </main>
{/key}