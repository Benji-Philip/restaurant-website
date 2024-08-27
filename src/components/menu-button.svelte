<script>
  export let buttonNumber;
  export let selectedButton;
</script>

<button on:click
  class=" border-[#281c1c] border-2 px-4 py-2 mx-4 text-[10px] md:text-[12px] hidden sm:block hover:scale-105 {selectedButton ===
  buttonNumber
    ? 'bg-[#281c1c] text-white'
    : 'text-[#281c1c] bg-white'}"><slot /></button
>
