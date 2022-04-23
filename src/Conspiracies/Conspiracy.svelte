<script lang="ts">
  export let id: string;
  export let location;
  export let navigation;

  interface Conspiracy {
    id: string;
    title: string;
    conspiracy: string;
  }

  import * as Conspiracies from "./Conspiracies.json";

  const conspiracy = (Conspiracies.conspiracies as Conspiracy[]).find(
    (con) => con.id === id
  );
</script>

<svelte:head><title>{conspiracy?.title ?? "Not found"}</title></svelte:head>

<div>
  <h1>{conspiracy.title}</h1>

  <p>{conspiracy.conspiracy}</p>
</div>
