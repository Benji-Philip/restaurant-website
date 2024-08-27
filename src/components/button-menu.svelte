<script>
  import { createEventDispatcher } from "svelte";
  import MenuButton from "./menu-button.svelte";
  const dispatch = createEventDispatcher();
  let selectedButton = 1;
  let count = 1;
  function click(number) {
    selectedButton = number;
    count += 1;
    console.log(count);
    dispatch("ButtonMenuEvent",{
      selected: selectedButton
    });
  }
</script>

<MenuButton {selectedButton} buttonNumber={1} on:click={() => click(1)}
  >Appetizers</MenuButton
>
<MenuButton {selectedButton} buttonNumber={2} on:click={() => click(2)}
  >Main Course</MenuButton
>
<MenuButton {selectedButton} buttonNumber={3} on:click={() => click(3)}
  >Desserts</MenuButton
>
<MenuButton {selectedButton} buttonNumber={4} on:click={() => click(4)}
  >Specials</MenuButton
>
