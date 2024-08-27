<script>
  import ImageTwo from "../assets/image-2.jpg"
  import ButtonMenu from "../components/button-menu.svelte";
  let selectedButton = 1;
  function handleButtonMenuEvent(e) {
    selectedButton = e.detail.selected;
  }
</script>

<div class="flex">
  <ButtonMenu on:ButtonMenuEvent={handleButtonMenuEvent}></ButtonMenu>
</div>
<div class="flex flex-row w-[70vw] flex-1 mt-10">
  <div class="flex flex-col flex-1 justify-center">
    <section class="hidden sm:block justify-start mr-6">
      <div class="flex flex-col text-left gap-6 w-full flex-1">
        {#if selectedButton === 1}
          <div class=" border-b-2 pb-3">Bruschetta al Pomodoro</div>
          <div class=" border-b-2 pb-3">Caprese Salad</div>
          <div class=" border-b-2 pb-3">Aranchini di Riso</div>
          <div class=" border-b-2 pb-3">Prosciutto e Melone</div>
          <div class=" border-b-2 pb-3">Burrata with Roasted Peppers</div>
        {/if}{#if selectedButton === 2}
          <div class=" border-b-2 pb-3">Fancy meal</div>
          <div class=" border-b-2 pb-3">Happy meal</div>
          <div class=" border-b-2 pb-3">idk eat piza</div>
          <div class=" border-b-2 pb-3">food?</div>
        {/if}{#if selectedButton === 3}
          <div class=" border-b-2 pb-3">chocolate ice-no-cream</div>
          <div class=" border-b-2 pb-3">icecream</div>
          <div class=" border-b-2 pb-3">pudding</div>
          <div class=" border-b-2 pb-3">yummy yum yum</div>
          <div class=" border-b-2 pb-3">wasabi</div>
        {/if}{#if selectedButton === 4}
          <div class=" border-b-2 pb-3">Big chicken</div>
          <div class=" border-b-2 pb-3">Big Beef</div>
          <div class=" border-b-2 pb-3">nino kuni</div>
        {/if}
      </div>
    </section>
  </div>
  <img
    src={ImageTwo.src}
    alt=""
    class="h-[300px] w-[300px] object-cover rounded-xl m-6 mr-0 hidden md:block"
  />
</div>
