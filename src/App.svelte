<script lang="ts">
  import { Router, Route } from "svelte-navigator";

  import Nav from "./Nav.svelte";
  import Home from "./Home.svelte";
  import Conspiracies from "./Conspiracies.svelte";
  import Conspiracy from "./Conspiracy.svelte";
  import Memes from "./Memes.svelte";
</script>

<Router>
  <Nav />

  <main>
    <Route path="/">
      <Home />
    </Route>

    <Route path="memes">
      <Memes />
    </Route>
    <Route path="conspiracies/*">
      <Route path="/">
        <Conspiracies />
      </Route>

      <Route path=":id" component={Conspiracy} />
    </Route>
  </main>
</Router>

<style>
  :global(body) {
    margin: 0 !important;
    padding: 0 !important;
  }

  main {
    display: grid;
    align-content: center;
    justify-content: center;
  }
</style>
