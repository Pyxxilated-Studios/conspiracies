<script lang="ts">
  import * as Memes from "./Memes.json";
  const { memes } = Memes;
</script>

<div class="memes">
  <!-- <ul> -->
  {#each memes as meme}
    <!-- <li> -->
    <img src={meme} alt="Ryan meme {meme}" />
    <!-- </li> -->
  {/each}
  <!-- </ul> -->
</div>

<style>
  .memes {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    grid-gap: 3em;
    grid-auto-flow: dense;
    margin: 3em;
  }
  .memes img {
    border-radius: 8px;
    box-shadow: 4px 4px 4px 4px;
    width: 100%;
    object-fit: contain;
  }
</style>
