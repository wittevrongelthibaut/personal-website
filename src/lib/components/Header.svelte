<script>
  import { page } from '$app/stores';
</script>
<header>
    <nav>
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
      </ul>
    </nav>
    
  </header>

  <style lang='scss'>
    $accentColor: #B0DDC2;
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
        margin-left: auto;
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
    </style>