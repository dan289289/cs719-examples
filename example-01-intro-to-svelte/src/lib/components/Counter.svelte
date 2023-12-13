<script>
    import CounterSquared from "./CounterSquared.svelte";

  /**
   * We will display this value as part of the button's text below.
   *
   * When this value changes, Svelte will automatically take care of re-rendering the button!
   * This is known as a Reactive value, or Reactive state.
   *
   * This is one of the main benefits of a framework like Svelte - it means we don't have to have
   * tonnes of messy code to update the UI in response to state changes - that part is handled for us :)
   */
  let count = 0;
</script>

<!-- The button displays the "count" value above, and increments it when clicked. -->

<div id="number-container">
  <button id="plus-btn" on:click={() => count++}>+</button>
  <input id="counter-text" type="text" value={count} readonly />
  <button id="minus-btn" on:click={() => count--}>-</button>
</div>

<CounterSquared count={count} />

<!-- Here's some random CSS. It will only apply to this component. -->
<style>
  button {
    border: 0;
    background-color: rgb(52, 154, 70);
    padding: 10px 0;
    translate: -1px -1px;
    box-shadow: 2px 2px 2px rgba(128, 128, 128, 0.5);
    color: white;
    font-weight: bold;
    width: 10%;
  }

  button:hover {
    background-color: rgb(97, 165, 90);
  }

  button:active {
    background-color: rgb(42, 139, 70);
    translate: 0;
    box-shadow: 1px 1px 2px rgba(128, 128, 128, 0.5);
  }

  #number-container {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    gap: 10px;
  }

  #counter-text {
    font-size: 20px;
    font-weight: bold;
    color:black;
    background-color: rgb(201, 232, 182);
    width: 20%;
    text-align: center;
  }

  

</style>
