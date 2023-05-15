<script>
	import { fly, scale } from 'svelte/transition';
  import { page } from '$app/stores';
  import { Hamburger } from 'svelte-hamburgers';
  import { quadOut } from 'svelte/easing';

  let open;
  
</script>
<header>

  <div id="mobile">
    <Hamburger bind:open --color=#B0DDC2 />

    {#if open}
      <nav id='mobile-nav'>
        <li transition:fly={{ y: -15, delay: 50}}>
          <a href="/">Home</a>
        </li>
        {#each ['About', 'Projects', 'Contact'] as link, i}
        <li transition:fly={{ y: -15, delay: 50 * i+1 }}>
          <a href="/#{link.toLowerCase()}">{link}</a>
        </li>
        {/each}
        <li transition:fly={{ y: -15, delay: 50 * 4}}>
          <a href="/blog">Blog</a>
        </li>
        <li transition:fly={{ y: -15, delay: 50 * 5}}>
          <a href="/files/CV_Wittevrongel_Thibaut.pdf" target="_blank">Resume</a>
        </li>
      </nav>
      <div class="bar" transition:scale={{ duration: 750, easing: quadOut, opacity: 1 }} />
    {/if}
  </div>
    <nav id='desktop'>
      <ul>
        <li>
          <a href="/">Home</a>
        </li>
        {#if $page.url.pathname == '/'}
        <li>
          <a href="/#about">About</a>
        </li>
        <li>
          <a href="/#projects">Projects</a>
        </li>
        <li>
          <a href="/#contact">Contact</a>
        </li>
        {/if}
        <li>
          <a href="/blog">Blog</a>
        </li>
        <li>
          <a href="/files/CV_Wittevrongel_Thibaut.pdf" target="_blank" >Resume</a>
        </li>
      </ul>
    </nav>
    
  </header>

  <style lang='scss'>
    $accentColor: #B0DDC2;
    #mobile {
      display: none;
      text-align: right;
    }
    #mobile-nav{
      list-style: none;
      li{
        text-align: center;
        margin-bottom: 1.5rem;
      }
    }
    .bar {
        border-style: solid;
        border-color: $accentColor;
        border-width: 1px;
        height: 0;
    }
    header {
      padding: 1rem;
      width: 100%;
    }
    ul {
      margin: 0;
      list-style-type: none;
      display: flex;
      li{
        border-left: 1px solid $accentColor;
        border-right: 1px solid $accentColor;
        padding: 0.5rem;
        margin-left: -1px;
      }
      li:nth-last-child(1) {
        border: none;
        margin-left: auto;
        a{
            border: $accentColor 1px solid;
            padding: 1rem;
            border-radius: 5px;
            margin-top: 1rem;
            margin-bottom: 1rem;
            &:hover{
                background-color: rgba(176, 221, 194, 0.2);;
                outline: none;
            }
            &::after{
                position: inherit;
            }
            &::hover::after{
                position: inherit;
            }
        }
      }

    }
    
    a {
      text-decoration: none;
      color: inherit;
      font-size: 1.2rem;
      font-weight: 700;
      padding: 1rem;
      &:hover {
        color: $accentColor;
      }
    }
    @media screen and (max-width: 30rem){
      #desktop{
        display: none;
      }
      #mobile{
        display: block;
      }
    }
    </style>