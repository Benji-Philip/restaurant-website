<script>
  import ImageOne from "../assets/image-1.webp";
  import ImageTwo from "../assets/image-2.webp";
  import ImageThree from "../assets/image-3.webp";
  import ImageFour from "../assets/image-4.webp";
  import ButtonMenu from "./button-menu.svelte";
  import Appetizers from "./appetizers.svelte";
  import MainCourse from "./main-course.svelte";
  import Desserts from "./desserts.svelte";
  import Specials from "./specials.svelte";
  import ImageOneSmall from "../assets/image-1-small.webp";
  import ImageTwoSmall from "../assets/image-2-small.webp";
  import ImageThreeSmall from "../assets/image-3-small.webp";
  import ImageFourSmall from "../assets/image-4-small.webp";
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
  <div
        class=" bg-cover bg-center h-[300px] w-[300px] object-cover rounded-xl m-6 mr-0 hidden md:block md:{selectedButton ===
    1
      ? 'block'
      : 'hidden'}"
        style="background-image: url({ImageTwoSmall.src})"
      ><img
    decoding="async"
    loading="lazy"
    src={ImageTwo.src}
    alt=""
    class="h-[300px] w-[300px] object-cover rounded-xl hidden md:block md:{selectedButton ===
    1
      ? 'block'
      : 'hidden'}"
  /></div>
  
  
  <div
        class="bg-cover bg-center h-[300px] w-[300px] object-cover rounded-xl m-6 mr-0 hidden md:block md:{selectedButton ===
    2
      ? 'block'
      : 'hidden'}"
        style="background-image: url({ImageOneSmall.src})"
      ><img
    decoding="async"
    loading="lazy"
    src={ImageOne.src}
    alt=""
    class="h-[300px] w-[300px] object-cover rounded-xl hidden md:block md:{selectedButton ===
    2
      ? 'block'
      : 'hidden'}"
  /></div>
  
  
  <div
        class="bg-cover bg-center h-[300px] w-[300px] object-cover rounded-xl m-6 mr-0 hidden md:block md:{selectedButton ===
    3
      ? 'block'
      : 'hidden'}"
        style="background-image: url({ImageFourSmall.src})"
      ><img
    decoding="async"
    loading="lazy"
    src={ImageFour.src}
    alt=""
    class="h-[300px] w-[300px] object-cover rounded-xl hidden md:block md:{selectedButton ===
    3
      ? 'block'
      : 'hidden'}"
  /></div>
  
  
  <div
        class="bg-cover bg-center h-[300px] w-[300px] object-cover rounded-xl m-6 mr-0 hidden md:block md:{selectedButton ===
    4
      ? 'block'
      : 'hidden'}"
        style="background-image: url({ImageThreeSmall.src})"
      ><img
    decoding="async"
    loading="lazy"
    src={ImageThree.src}
    alt=""
    class="h-[300px] w-[300px] object-cover rounded-xl hidden md:block md:{selectedButton ===
    4
      ? 'block'
      : 'hidden'}"
  /></div>
</div>