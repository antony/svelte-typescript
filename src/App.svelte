<script lang="ts">
  import myStore from './stores'
  import Sub from './Sub.svelte'
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  {#each $myStore as storedName}
  <h1>Hello {storedName.name}!</h1>
  {/each}
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
  <Sub on:ev={e => console.log(e.detail.my)}/>
</main>
