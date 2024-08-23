<script lang="ts">
  import { onMount } from "svelte";

  let currentText = "";
  const sentences = [
    "Ready to Launch Your Project or Business Idea?",
    "Is it a website?",
    "Is it a mobile application?",
    "Or is it a desktop application?",
    "We got you covered!",
    "You are in the right place...",
  ];
  let sentenceIndex = 0;
  let charIndex = 0;
  let isDeleting = false;

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
  });
</script>

<main class="w-full h-full">
  <div class="flex flex-col md:flex-row w-full">
    <div
      class="w-full md:w-1/2 bg-[#5454D4] rounded-[5px] flex justify-center items-center text-center m-4 h-full clip-path text-3xl p-8 md:p-16 text-white"
    >
      <p class="jersey p-3 max-md:w-max max-md:h-[6rem] w-max h-[7rem]">
        {currentText}
      </p>
    </div>
    <div class="w-full md:w-1/2 flex justify-center items-center">
      <img
        src="/woman-photo-removebg.png"
        alt="woman-img"
        class="w-full h-auto max-w-xs md:max-w-full"
      />
    </div>
  </div>
</main>
