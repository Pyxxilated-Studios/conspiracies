<script lang="ts">
  import * as Memes from "./Memes.json";
  const { memes } = Memes;
</script>

<div class="memes">
  {#each memes as meme}
    <img src={meme} alt="Ryan meme {meme}" width="300" height="400" />
  {/each}
</div>

<style>
  .memes {
    display: grid;
    grid-template-columns: auto auto auto;
  }

  .memes > img {
    margin: 2em;
    border-radius: 8px;
    box-shadow: 4px 4px 4px 4px;
  }

  .memes > img:hover {
    scale: 1.2;
  }
</style>
