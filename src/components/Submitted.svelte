<script>
  import thankYouSVG from "../assets/illustration-thank-you.svg";
  export let rating;
</script>

<main>
  <div class="holder" style="justify-content: space-around;">
    <img src={thankYouSVG} alt="mySVG" class="thank-you-image" />
    <div class="rating-display">You selected {rating} out of 5</div>
    <h1 style="align-self:center">Thank you!</h1>
    <p class="holder-text" style="text-align: center;">
      We appreciate you taking the time to give a rating. If you ever need more
      support, don’t hesitate to get in touch!
    </p>
  </div>
</main>
