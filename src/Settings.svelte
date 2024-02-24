<script>
  import { fade, fly } from "svelte/transition";
  import { nav, user, chatTopic } from "./stores.js";
  import { flip } from "svelte/animate";
  import Input from "./ui/Input.svelte";
</script>

<main>
  <form
    on:submit|preventDefault={e => {
      if (!$user) return;
      $nav = 'messages';
    }}
  >
    <label id="name-label">nickname</label>
    <Input
      bind:value={$user}
      maxLength="50"
      placeholder="sudo-self"
      ariaLabelledBy="name-label"
    />
    <label id="chat-label">topic</label>
    <Input
      bind:value={$chatTopic}
      maxLength="50"
      placeholder="chat topic"
      ariaLabelledBy="chat-label"
    />
  </form>
</main>

<style>
  main {
    margin: auto 0;
  }

  form {
    padding: 2em;
  }

  label {
    padding: 1em;
    font-size: 14px;
  }
</style>
