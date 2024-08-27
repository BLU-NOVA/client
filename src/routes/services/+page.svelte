<script>
  import Icon from "@iconify/svelte";
</script>

<main class="overflow-x-hidden mt-[4rem] px-4 md:px-8 lg:px-16">
  <div class="flex flex-col lg:flex-row gap-8">
    <div class="lg:flex-1">
      <div class="text-white text-4xl sm:text-5xl lg:text-7xl p-3">
        <div class="w-full lg:w-max">
          Let Our <span class="text-electric-blue">Experts</span>
          <br /> Build Your <span class="text-electric-blue"> Website</span>.
        </div>
      </div>
      <div class="p-3">
        <p
          class="text-white text-wrap text-xl sm:text-2xl font-light w-full lg:w-[70%]"
        >
          Our team creates custom website themes, Mobile Apps and Desktop
          applications either you have a design or not.
        </p>
      </div>
    </div>
    <div class="lg:flex-1 relative h-[300px] sm:h-[400px] lg:h-[600px]">
      <img
        src="/web-1.png"
        alt="showcase-1"
        class="absolute top-4 right-4 z-10 w-3/4 lg:w-auto"
      />
      <img
        src="/web-2.png"
        alt="showcase-2"
        class="absolute top-20 left-0 lg:left-[5rem] z-20 w-3/4 lg:w-auto"
      />
    </div>
  </div>
  <div class="mt-12 mb-6">
    <p class="text-electric-blue text-center text-2xl sm:text-3xl mb-8">
      Our Services
    </p>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
      <!-- Service 1 -->
      <div class="text-center">
        <div class="flex justify-center items-center">
          <Icon
            icon="pixelarticons:circle"
            class="text-electric-blue text-4xl sm:text-5xl mb-4"
          />
        </div>
        <h3 class="text-white text-lg sm:text-xl">Design</h3>
        <p class="text-gray-300 mt-2 text-sm sm:text-base">
          We create a unique web design reflecting your brand & graphic
          guidelines.
        </p>
      </div>
      <!-- Service 2 -->
      <div class="text-center">
        <div class="flex justify-center items-center">
          <Icon
            icon="mdi:code"
            class="text-electric-blue text-4xl sm:text-5xl mb-4"
          />
        </div>
        <h3 class="text-white text-lg sm:text-xl">Development</h3>
        <p class="text-gray-300 mt-2 text-sm sm:text-base">
          We turn the design into a theme, making it easy to update to new
          versions.
        </p>
      </div>
      <!-- Service 3 -->
      <div class="text-center">
        <div class="flex justify-center items-center">
          <Icon
            icon="clarity:slider-line"
            class="text-electric-blue text-4xl sm:text-5xl mb-4"
          />
        </div>
        <h3 class="text-white text-lg sm:text-xl">Implementation</h3>
        <p class="text-gray-300 mt-2 text-sm sm:text-base">
          We help you setting-up your online store. (categories, products,
          pricelists...)
        </p>
      </div>
      <!-- Service 4 -->
      <div class="text-center">
        <div class="flex justify-center items-center">
          <Icon
            icon="la:user-cog"
            class="text-electric-blue text-4xl sm:text-5xl mb-4"
          />
        </div>
        <h3 class="text-white text-lg sm:text-xl">Training</h3>
        <p class="text-gray-300 mt-2 text-sm sm:text-base">
          We provide training for you to become autonomous to update it.
        </p>
      </div>
    </div>
  </div>
</main>

<style>
  @media (max-width: 1023px) {
    .relative img {
      max-width: 80%;
      height: auto;
    }
  }
</style>
