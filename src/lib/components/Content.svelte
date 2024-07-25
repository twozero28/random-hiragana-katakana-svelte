<script>
  import Character from "./Character.svelte";
  import Pronunciation from "./Pronunciation.svelte";
  import {getRandomCharacter} from "../utils/get-random-character.js";
  import {hiraganas, katakanas} from "../data/charaters.js";

  let character = getRandomCharacter([...hiraganas, ...katakanas]);
</script>

<div>
  <Character value={character.problem}/>
  <Pronunciation value={character.answer}/>
</div>

<style>
  div {
    position: relative;
    user-select: none;
    text-align: center;
  }
</style>