<script lang="ts">
  import * as Conspiracies from "./Conspiracies.json";

  const { conspiracies } = Conspiracies;
</script>

<ol>
  {#each conspiracies as conspiracy}
    <li>
      <a href="conspiracies/{conspiracy.id}">
        {conspiracy.title}
      </a>
    </li>
  {/each}
</ol>
