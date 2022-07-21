<script lang="ts">
import { css } from '@emotion/css'

export let label: string;
export let outlined: boolean = false;
export let fluid: boolean = false;

const styles = css`
  background-color: ${!outlined ? 'var(--bright-blue)' : 'transparent'};
  width: ${!fluid ? 'unset' : '100%'};

  p {
    color: ${!outlined ? 'white' : 'black'};
  }

  &:hover {
    opacity: .8;
    box-shadow: ${!outlined ? 'rgba(0, 0, 0, 0.1) 0px 10px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px' : 'unset'};
  }
`
</script>

<button class="{styles}" title={label}>
  <p>{label}</p>
</button>

<style lang="scss">
  button {
    padding: .8rem 1.6rem;
    color: white;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    opacity: .7;
    transition: .2s ease-in-out;

    p {
      font-size: 14px;
      font-weight: 700;
    }
  }
</style>