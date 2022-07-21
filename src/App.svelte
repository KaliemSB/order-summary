<script lang="ts">
import Button from "./components/Button.svelte";
import Plan from "./components/Plan.svelte";
import image from "./static/images/illustration-hero.svg"

const value: number = 59.99
</script>
<main>
  <div class="card">
    <img src={image} alt="Illustration">
    <div class="text">
      <h1>Order Summary</h1>
      <p>You can now listen to millions of songs, audiobooks, and podcasts on any device anywhere you like!</p>
      <Plan price={value} />
      <Button label="Proceed to Payment" fluid/>
      <Button label="Cancel Order" outlined fluid/>
    </div>
  </div>
</main>

<style lang="scss" scoped>
main {
  width: 100vw;
  height: 100vh;
  display: grid;
  place-items: center;

  .card {
    margin: 0 5%;
    max-width: 400px;
    background: white;
    border-radius: 18px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;

    img {
      width: 100%;
      border-radius: 18px 18px 0 0;
    }

    .text {
      text-align: center;
      display: grid;
      place-items: center;
      max-width: 65%;
      margin: 2rem auto;
      gap: 1rem;

      h1 {
        font-size: 1.6rem;
        font-weight: 900;
        color: var(--dark-blue);
      }

      p {
        color: var(--desaturated-blue);
      }
    }
  }
}
</style>