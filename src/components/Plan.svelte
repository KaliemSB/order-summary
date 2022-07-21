<script lang="ts">
export let price: number;
</script>

<div class="button">
  <div class="plan">
    <img src="/src/static/images/icon-music.svg" alt="Music">
    <div>
      <p>Annual Plan</p>
      <span>${price}/year</span>
    </div>
  </div>
  <a href="/">Change</a>
</div>

<style lang="scss" scoped>
.button {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background: var(--very-pale-blue);
  padding: .8em 1.2em;
  border-radius: 12px;

  .plan {
    display: flex;
    align-items: center;
    gap: .8em;
    user-select: none;

    img {
      width: 26%;
    }

    div {
      text-align: start;

      p {
        font-weight: 700;
        font-size: 14px;
        color: var(--dark-blue);
      }

      span {
        font-weight: 400;
        font-size: 12px;
        color: var(--desaturated-blue);
      }
    }
  }

  a {
    color: var(--bright-blue);
    font-size: 12px;
    opacity: .8;

    &:hover {
      opacity: 1;
    }
  }
}
</style>