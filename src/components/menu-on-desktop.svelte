<script>
  import ButtonMenu from "./button-menu.svelte";
  import Appetizers from "./appetizers.svelte";
  import MainCourse from "./main-course.svelte";
  import Desserts from "./desserts.svelte";
  import Specials from "./specials.svelte";
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
          <Appetizers />
        {/if}{#if selectedButton === 2}
          <MainCourse />
        {/if}{#if selectedButton === 3}
          <Desserts />
        {/if}{#if selectedButton === 4}
          <Specials />
        {/if}
      </div>
    </section>
  </div>
</div>
