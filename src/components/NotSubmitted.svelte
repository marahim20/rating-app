<script>
  import { createEventDispatcher } from "svelte";
  import iconStar from "../assets/icon-star.svg";
  let rating;
  const dispatch = createEventDispatcher();
  const handleClick = (e) => {
    dispatch("submit", rating);
  };
  const handleRating = (e) => {
    rating = e.target.innerText;
  };
</script>

<main>
  <div class="holder">
    <div class="star">
      <img src={iconStar} alt="star" />
    </div>
    <h1>How did we do?</h1>
    <p class="holder-text">
      Please let us know how we did with your support request. All feedback is
      appreciated to help us improve our offering!
    </p>
    <div class="button-holder">
      <button class="number" on:click={handleRating}>1</button>
      <button class="number" on:click={handleRating}>2</button>
      <button class="number" on:click={handleRating}>3</button>
      <button class="number" on:click={handleRating}>4</button>
      <button class="number" on:click={handleRating}>5</button>
    </div>
    <button class="submit-button" on:click={handleClick}>SUBMIT</button>
  </div>
</main>
