<script lang="ts">
  interface Conspiracy {
    id: string;
    title: string;
    conspiracy: string;
  }

  import * as Conspiracies from "./Conspiracies/Conspiracies.json";

  const conspiracies = Conspiracies.conspiracies as Conspiracy[];
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
