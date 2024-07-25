<script>
  import GithubIcon from "./GithubIcon.svelte";

  let isAuto = true;

  let character = 'both';

  let time = 2.5;
  const times = [1, 1.5, 2, 2.5, 3, 3.5, 4, 4.5, 5];

</script>

<nav class="bar">
  <div class="condition-container">
    <div>
      <input id="autoCheckBox" type="checkbox" bind:checked={isAuto} />
      <label for="autoCheckBox">Auto</label>
    </div>
    <div>
      <select bind:value={character}>
        <option value="both">Both</option>
        <option value="hiragana">Hiragana</option>
        <option value="Katakana">Katakana</option>
      </select>
    </div>
    <div>
      <select bind:value={time}>
        {#each times as t}
          <option value={t}>{t}</option>
        {/each}
      </select>
    </div>
  </div>
  <GithubIcon/>
</nav>

<style>
  .bar {
    padding: 8px 12px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  label {
    cursor: pointer;
  }

  .condition-container {
    display: flex;
    align-items: center;
    column-gap: 0.5rem;
  }

  .condition-container > div {
    display: flex;
    align-items: center;
  }

  #autoCheckBox {
    margin-right: 4px;
  }

</style>