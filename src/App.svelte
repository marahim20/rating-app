<script>
  import NotSubmitted from "./components/NotSubmitted.svelte";
  import Submitted from "./components/Submitted.svelte";
  import css from "./assets/style.css";
  const handleSubmit = (e) => {
    submit = true;
    rating = e.detail;
  };
  let rating;
  $: submit = false;
</script>

<main>
  {#if !submit}
    <NotSubmitted on:submit={handleSubmit} />
  {:else}
    <Submitted {rating} />
  {/if}
</main>
