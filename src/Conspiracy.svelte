<script lang="ts">
  import * as Conspiracies from "./Conspiracies.json";

  export let id: string;

  const conspiracy = Conspiracies.conspiracies.find((con) => con.id === id);
</script>

<svelte:head><title>{conspiracy?.title ?? "Not found"}</title></svelte:head>

<div>
  <h1>{conspiracy?.title ?? "No such conspiracy was written by Ryan"}</h1>

  {#if conspiracy}
    <p>{conspiracy.conspiracy}</p>
  {/if}
</div>
