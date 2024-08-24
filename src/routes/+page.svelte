<script lang="ts">
  import Chart from "$lib/Chart.svelte";
  import DisplayCard from "$lib/DisplayCard.svelte";
  import GrowthArrow from "$lib/GrowthArrow.svelte";
  import Join from "$lib/Join.svelte";
  import { onMount } from "svelte";

  import { slide } from "svelte/transition";

  let currentText = "";
  const sentences = [
    "Ready to Launch Your Project or Bizz?",
    "Is it a website?",
    "Is it a mobile application?",
    "Or is it a desktop application?",
    "We got you covered!",
    "You are in the right place...",
  ];
  let sentenceIndex = 0;
  let charIndex = 0;
  let isDeleting = false;
  let showContent = true; // To control visibility

  function typeText() {
    if (isDeleting) {
      // Deleting text
      if (charIndex > 0) {
        currentText = currentText.slice(0, -1);
        charIndex--;
        setTimeout(typeText, 50); // Adjust deleting speed here (50ms)
      } else {
        // Switch to next sentence after deletion
        isDeleting = false;
        sentenceIndex = (sentenceIndex + 1) % sentences.length;
        setTimeout(typeText, 500); // Adjust pause duration here (500ms)
      }
    } else {
      // Typing text
      if (charIndex < sentences[sentenceIndex].length) {
        currentText += sentences[sentenceIndex].charAt(charIndex);
        charIndex++;
        setTimeout(typeText, 100); // Adjust typing speed here (100ms)
      } else {
        isDeleting = true;
        setTimeout(typeText, 2000); // Adjust pause duration here (2 seconds)
      }
    }
  }

  onMount(() => {
    typeText();
    // const handleScroll = () => {
    //   if (window.scrollY > 200) {
    //     // Adjust scroll distance as needed
    //     showContent = false;
    //   } else {
    //     showContent = true;
    //   }
    // };
    // window.addEventListener("scroll", handleScroll);
    // return () => {
    //   window.removeEventListener("scroll", handleScroll);
    // };
  });
</script>

<main class="w-full">
  {#if showContent}
    <div
      class="flex flex-col md:flex-row w-full"
      in:slide={{ duration: 400, delay: 200 }}
      out:slide={{ duration: 400 }}
    >
      <div
        class="w-full md:w-1/2 bg-[#5454D4] rounded-[5px] flex justify-center items-center text-center m-4 h-full clip-path text-3xl p-8 md:p-16 text-white"
      >
        <p class="jersey p-3 max-md:w-max max-md:h-[6rem] w-max h-[7rem] m-3">
          {currentText}
        </p>
      </div>
      <div
        class="w-full md:w-1/2 mt-[20%] flex justify-center items-center p-4"
      >
        <img
          src="/woman-photo-removebg.png"
          alt="woman-img"
          class="w-full h-auto max-w-xs md:max-w-full p-3 rounded-[12px] bg-yellow-600 shadow-lg"
        />
      </div>
    </div>
  {/if}
  <div class="p-3">
    <p class="text-center text-3xl font-bold text-electric-blue">WHAT WE DO!</p>
    <DisplayCard />
  </div>
  <div class="p-3">
    <p class="text-center text-2xl text-electric-blue font-bold">WHY US?</p>
    <div class="text-white">
      <Chart />
    </div>
  </div>
  <div class="flex justify-center items-center flex-col">
    <GrowthArrow />
    <p class="text-white font-extralight line-through text-center">
      Struggle to migrate or manage your business online.
    </p>
    <p class="text-white font-bold text-2xl text-center">
      Watch your business grow and scale online with us.
    </p>
  </div>
  <div class="mt-4 flex justify-center items-center">
    <Join />
  </div>
</main>
