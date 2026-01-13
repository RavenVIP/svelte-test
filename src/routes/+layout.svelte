<script>
  let dark = false;
</script>

<nav
  style="display:flex; gap:12px; padding:12px; border-bottom:1px solid #ddd;"
>
  <a href="/">Home</a>
  <a href="/about">About</a>

  <button on:click={() => (dark = !dark)} style="margin-left:auto">
    {dark ? "Light" : "Dark"}
  </button>
</nav>

<main
  style="
    padding:16px;
    min-height:100vh;
    background: {dark ? '#111' : '#fff'};
    color: {dark ? '#eee' : '#000'};
  "
>
  <slot />
</main>
