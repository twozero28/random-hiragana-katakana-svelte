<script>
  import NavBar from "./lib/components/NavBar.svelte";
  import Content from "./lib/components/Content.svelte";
</script>

<header>
  <NavBar/>
</header>

<main>
  <Content/>
</main>

<style>
  header {
    width: 100vw;
    position: fixed;
  }

  main {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
