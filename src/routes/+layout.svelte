<script>
  import "../app.css";
  import Navbar from "$lib/Navbar.svelte";
  import Footer from "$lib/Footer.svelte";
</script>

<main class="flex flex-col bg-deep-space-blue">
  <div class="  h-[20%]">
    <Navbar />
  </div>
  <div class="bg-[#1B264C]">
    <slot />
  </div>
  <Footer />
</main>
