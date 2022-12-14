<script>
  import '../style/_index.scss'
</script>

<svelte:head>
  <title>Frontend Design & Development | Creative Coding</title>
</svelte:head>
  
<main>
  <header>
    <nav>
      <ul>
        <li>
          <a href="/">
            Basics
          </a>
        </li>
        <li>
          <a href="/scrolltrigger">
            ScrollTrigger
          </a>
        </li>
        <li>
          <a href="/flip">
            Flip
          </a>
        </li>
      </ul>
    </nav>
  </header>
    <slot />
</main>


<style lang="scss">
  header {
    position: fixed;
    right: 0;
    ul {
      display: flex;
      justify-content: flex-end;
      gap: 2rem;
      padding: 1.25rem 2rem;
      list-style: none;
      font-family: sans-serif;
    }
    a {
      text-decoration: none;
      color: inherit;
    }
  }
</style>