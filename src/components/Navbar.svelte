<script lang="ts">
  let isMenuOpen: boolean = false;

  const toggleMenu = () => {
    isMenuOpen = !isMenuOpen;
  };
</script>

<nav class="bg-deep-space-blue text-nova-white p-4">
  <div class={`container mx-auto flex flex-wrap justify-between `}>
    <div class={`flex  ${isMenuOpen ? "max-md:hidden" : ""}`}>
      <img
        src="/blu-bgless.png"
        alt="icon"
        class="w-[40px] h-[40px] sm:w-[50px] sm:h-[50px] animate-spin"
      />
      <div class={`text-electric-blue font-bold text-lg sm:text-xl sm:mt-2`}>
        BLU NOVA
      </div>
    </div>

    <div class="block sm:hidden">
      <button
        on:click={toggleMenu}
        class="text-electric-blue focus:outline-none"
      >
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          ></path>
        </svg>
      </button>
    </div>

    <ul
      class={`sm:flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-6 mt-4 sm:mt-0 ${isMenuOpen ? "block" : "hidden"}`}
    >
      <li class="hover:text-comet-cyan py-2 px-4 rounded bg-deep-space-blue">
        Home
      </li>
      <li class="hover:text-comet-cyan py-2 px-4 rounded bg-deep-space-blue">
        About
      </li>
      <li class="hover:text-comet-cyan py-2 px-4 rounded bg-deep-space-blue">
        Services
      </li>
      <li class="hover:text-comet-cyan py-2 px-4 rounded bg-deep-space-blue">
        Contact
      </li>
    </ul>

    <div class="hidden sm:block">
      <button
        class="bg-[#5454D4] text-nova-white py-2 px-4 rounded hover:bg-nebula-purple transition"
      >
        Get Started
      </button>
    </div>
  </div>
</nav>
